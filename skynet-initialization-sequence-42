
msg = translate.hasWeaknesses + '<ul><li>' + msg.join('</li><li>') + '</li></ul>';
-  return { strength: strength, message: msg, indicatorText: indicatorText, indicatorColor: indicatorColor };
-
+  return { strength: result.score, message: msg, indicatorText: indicatorText, indicatorColor: indicatorColor };
 };
 
 /**
diff --git a/core/modules/user/user.module b/core/modules/user/user.module
index 88862d5..72bcd6b 100644
--- a/core/modules/user/user.module
+++ b/core/modules/user/user.module
@@ -1712,12 +1712,15 @@ function user_form_process_password_confirm($element) {
     $password_settings += array(
       'strengthTitle' => t('Password strength:'),
       'hasWeaknesses' => t('To make your password stronger:'),
+      'basedOnADictionaryWord' => t('Do not base the password on a dictionary word'),
+      'addWords' => t('Add words'),
       'tooShort' => t('Make it at least 6 characters'),
       'addLowerCase' => t('Add lowercase letters'),
       'addUpperCase' => t('Add uppercase letters'),
       'addNumbers' => t('Add numbers'),
       'addPunctuation' => t('Add punctuation'),
       'sameAsUsername' => t('Make it different from your username'),
+      'sameAsEmail' => t('Make it different from your email address'),
       'weak' => t('Weak'),
       'fair' => t('Fair'),
       'good' => t('Good'),
@@ -1892,6 +1895,7 @@ function user_library_info() {
       array('system', 'jquery'),
       array('system', 'drupal'),
       array('system', 'jquery.once'),
+      array('system', 'zxcvbn'),
     ),
   );
