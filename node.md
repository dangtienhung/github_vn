#terms

repository (Repo): -> là dự án của ta đang làm việc
Branch
Conflict
Local

1. git init -> để biến dự án của chúng ta trở thành 1 repository
2. git status -> cho ta thấy được trạng thái của mình
3. git add -> lưu lại dự án của file đó
   => cú pháp
   git add + tên file cần lưu
   git adđ . -> lưu tất cả các file cùng 1 lúc
4. git reset -> đẩy các file về trang thái chưa lưu
5. git commit -> ghi chú của file
   => cú pháp:
   git commit -m 'initial commit' -> đánh dấu lần đầu khi bắt đầu dự án
   git commit -m 'tên commit'
6. git log -> coi lại thời điểm lưu
   git log --oneline -> nó sẽ gọn gàng hơn
7. git checkout -> trỡ lại lần trước
   => cú pháp:
   git checkout + mã id -> cần quay trở lại lần trước
   git checkout master -> quay trở về hiện tại
8. git checkout {branch name} -> quay trở về nhành mình muốn hiện tại
9. git branch -> xem được cành mặc định của chúng ta
10. git chekout -b -> tạo ra brach mới
    => cú pháp:
    git chekout -b + tên branch muốn tạo
11. git checkout {branch name} -> di chuyển giữa các branch
    ex: git checkout master -> quay trở lại branch master
12. git merge {branch name} -> tổng hợp 2 branch lại thành 1
13. git branch -d {branch name} -> xóa đi 1 branch
14. git push -> đẩy lên local repo của mình
    => cú pháp:
    git push + đường link repository + tên branch
15. git remote add + {tên mình muốn đặt} + {link repository}
    -> cách tại ra tên thay thế cho link repository
16. git clone {link repository}
    => lấy 1 remote repo trên github về local của máy chúng ta (thông thường sẽ xảy ra nhiều hơn)
17. git stash
    => lưu lại trạng thái thay đổi => làm cho file register thay đổi trạng thái ban đầu
    => sau khi stash xong sẽ đánh dấu lại vị trí mà ta đánh dấu
18. git stash list
    => xem ra tất cả danh sách các stash
19. git stash list -p
    => xem chi tiết các thay đổi stash
20. git stash show + tên stash + -p
    ex: git stash show stash{0} -p
    => xem chi tiết của 1 statsh cụ thể
21. git stash apply + tên stash
    ex: git stash apply stash{0}
    => sử dụng stash cụ thể
    22: git stash drop + tên stash
    ex: git stash drop stash{0}
    => xóa đi 1 stash không cần dùng nữa
22. git stash clear
    => xóa hết các stash đi

---

\*\*\* tạo ra 1 branch ở local và đẩy lên repository
b1. tạo 1 branch mới ở local
b2. git push -u {link repository} + {name branch}

\*\*\* lấy ra 1 repo trên github đẩy về local
b1. trên máy local chúng ta dùng
=> git checkout master -> di chuyển về nhánh master
b2. git fetch origin
b3. git checkout -b {tên branch muốn tạo} origin/{tên branch trên git muốn lấy xuống}

\*\*\* kết hợp với git merge or với các branch khác
b1. git checkout master -> để trở về nhánh chính
b2. git pull -> để về những barnch

\*\*\* cách để git khôn theo dõi file nào đó
b1. tạo ra 1 file mới
=> cú pháp:
. + {tên file}
