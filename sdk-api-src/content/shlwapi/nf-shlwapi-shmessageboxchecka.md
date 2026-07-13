---
UID: NF:shlwapi.SHMessageBoxCheckA
title: SHMessageBoxCheckA function (shlwapi.h)
description: SHMessageBoxCheck may be altered or unavailable. (ANSI)
helpviewer_keywords: ["MB_ICONEXCLAMATION", "MB_ICONHAND", "MB_ICONINFORMATION", "MB_ICONQUESTION", "MB_OK", "MB_OKCANCEL", "MB_YESNO", "SHMessageBoxCheckA", "shlwapi/SHMessageBoxCheckA"]
old-location: shell\SHMessageBoxCheck.htm
tech.root: shell
ms.assetid: 7e62cde0-2b9f-44d3-afb8-5df71f98453a
ms.date: 12/05/2018
ms.keywords: MB_ICONEXCLAMATION, MB_ICONHAND, MB_ICONINFORMATION, MB_ICONQUESTION, MB_OK, MB_OKCANCEL, MB_YESNO, SHMessageBoxCheck, SHMessageBoxCheck function [Windows Shell], SHMessageBoxCheckA, SHMessageBoxCheckW, _win32_SHMessageBoxCheck, shell.SHMessageBoxCheck, shlwapi/SHMessageBoxCheck, shlwapi/SHMessageBoxCheckA, shlwapi/SHMessageBoxCheckW
req.header: shlwapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: SHMessageBoxCheckW (Unicode) and SHMessageBoxCheckA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shlwapi.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - SHMessageBoxCheckA
 - shlwapi/SHMessageBoxCheckA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shlwapi.dll
api_name:
 - SHMessageBoxCheck
 - SHMessageBoxCheckA
 - SHMessageBoxCheckW
---

# SHMessageBoxCheckA function


## -description

<p class="CCE_Message">[<b>SHMessageBoxCheck</b> is available for use in the operating systems specified in the Requirements section. It may be altered or unavailable in subsequent versions.]

Displays a message box that gives the user the option of suppressing further occurrences. If the user has already opted to suppress the message box, the function does not display a dialog box and instead simply returns the default value.

## -parameters

### -param hwnd [in, optional]

Type: <b>HWND</b>

The window handle to the message box's owner. This value can be <b>NULL</b>.

### -param pszText [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the message to be displayed.

### -param pszCaption [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains the title of the message box. If this parameter is set to <b>NULL</b>, the title is set to <b>Error!</b>.

### -param uType

Type: <b>UINT</b>

The flags that specify the contents and behavior of the message box. This function supports only a subset of the flags supported by <a href="/windows/desktop/api/winuser/nf-winuser-messagebox">MessageBox</a>. If you use any flags that are not listed below, the function's behavior is undefined.


You must specify the buttons to be displayed by setting one and only one of the following flags.





#### MB_OKCANCEL

Display a message box with <b>OK</b> and <b>Cancel</b> buttons.



#### MB_YESNO

Display a message box with <b>Yes</b> and <b>No</b> buttons.



#### MB_OK

Display a message box with an <b>OK</b> button.


You can display an optional icon by setting one and only one of the following flags.





#### MB_ICONHAND

Display a stop-sign icon.



#### MB_ICONQUESTION

Display a question-mark icon.



#### MB_ICONEXCLAMATION

Display an exclamation-point icon.



#### MB_ICONINFORMATION

Display an icon with a lowercase "i" in a circle.

### -param iDefault

Type: <b>int</b>

The value that the function returns when the user has opted not to have the message box displayed again. If the user has not opted to suppress the message box, the message box is displayed and the function ignores <i>iDefault</i>.

### -param pszRegVal [in]

Type: <b>LPCTSTR</b>

A pointer to a null-terminated string that contains a unique string value to associate with this message. To avoid collisions with values used by Microsoft, this string should include a GUID. This string must not exceed REGSTR_MAX_VALUE_LENGTH characters in length, including the terminating null character.

## -returns

Type: <b>int</b>

If the user has already chosen to suppress the message box, the function immediately returns the value assigned to <i>iDefault</i>.

If the user clicks the <b>OK</b>, <b>Cancel</b>, <b>Yes</b>, or <b>No</b> button, the function returns IDOK, IDCANCEL, IDYES, or IDNO, respectively.

If the user closes the message box by clicking the <b>X</b> button in the caption, the function returns IDCANCEL. This value is returned in this case even if the MB_OKCANCEL flag has not been set.

If an error occurs, the return value is normally –1. However, under certain low-memory conditions, the function might return <i>iDefault</i>.

## -remarks

<b>Security Warning:  </b>Do not take any dangerous actions if the function returns either –1 or <i>iDefault</i>. If an error occurs when attempting to display the message box, <b>SHMessageBoxCheck</b> returns –1 or, in some cases, <i>iDefault</i>. Such errors can be caused by insufficient memory or resources.  If you get one of these return values, you should be aware that the user did not necessarily see the dialog box and consequently did not positively agree to any action.

Do not confuse "Do not show this dialog box" with "Remember this answer". <b>SHMessageBoxCheck</b> does not provide "Remember this answer" functionality. If the user chooses to suppress the message box again, the function does not preserve which button they clicked. Instead, subsequent invocations of <b>SHMessageBoxCheck</b> simply return the value specified by <i>iDefault</i>. Consider the following example.
			
            	


```

int iResult = SHMessageBoxCheck(hwnd, 
                                TEXT("Do you want to exit without saving?"),
                                TEXT("Warning"), 
                                MB_YESNO, 
                                IDNO,
                                TEXT("{d9108ba3-9a61-4398-bfbc-b02102c77e8a}");
```


If the user selects <b>In the future, do not show me this</b> dialog box and clicks the <b>Yes</b> button, <b>SHMessageBoxCheck</b> returns IDYES. However, the next time this code is executed, <b>SHMessageBoxCheck</b> does not return IDYES, even though the user selected <b>Yes</b> originally. Instead, it returns IDNO, because that is the value specified by <i>iDefault</i>.

The default button displayed by the message box should agree with your <i>iDefault</i> value. The lack of support for the MB_DEFBUTTON2 flag means that <i>iDefault</i> should be set to IDOK if you have specified the MB_OK or MB_OKCANCEL flag. The <i>iDefault</i> value should be set to IDYES if you have set the MB_YESNO flag.

<b>SHMessageBoxCheck</b> records the message boxes that the user has chosen to suppress under the following registry key:
                
<pre><b>HKEY_CURRENT_USER</b>
   <b>Software</b>
      <b>Microsoft</b>
         <b>Windows</b>
            <b>CurrentVersion</b>
               <b>Explorer</b>
                  <b>DontShowMeThisDialogAgain</b></pre>





> [!NOTE]
> The shlwapi.h header defines SHMessageBoxCheck as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
