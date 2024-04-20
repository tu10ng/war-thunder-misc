# WAR THUNDER MISC

this will be the website of my personal war thunder thoughts.

# format
currently i will write this in emacs orgmode

# todo
- turn into web page

(defun browse-file-directory ()
  "Open the current file's directory however the OS would."
  (interactive)
  (if default-directory
      (browse-url-of-file (expand-file-name default-directory))
    (error "No `default-directory' to open")))

(shell-command (concat "start explorer /e,/select,\"" (replace-regexp-in-string "/" "\\\\" (buffer-file-name)) "\""))
