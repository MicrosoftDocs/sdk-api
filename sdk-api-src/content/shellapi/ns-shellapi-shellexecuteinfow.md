---
UID: NS:shellapi._SHELLEXECUTEINFOW
title: SHELLEXECUTEINFOW (shellapi.h)
description: Contains information used by ShellExecuteEx. (Unicode)
helpviewer_keywords: ["*LPSHELLEXECUTEINFOW","LPSHELLEXECUTEINFO","LPSHELLEXECUTEINFO structure pointer [Windows Shell]","SEE_MASK_ASYNCOK","SEE_MASK_CLASSKEY","SEE_MASK_CLASSNAME","SEE_MASK_CONNECTNETDRV","SEE_MASK_DEFAULT","SEE_MASK_DOENVSUBST","SEE_MASK_FLAG_DDEWAIT","SEE_MASK_FLAG_HINST_IS_SITE","SEE_MASK_FLAG_LOG_USAGE","SEE_MASK_FLAG_NO_UI","SEE_MASK_HMONITOR","SEE_MASK_HOTKEY","SEE_MASK_ICON","SEE_MASK_IDLIST","SEE_MASK_INVOKEIDLIST","SEE_MASK_NOASYNC","SEE_MASK_NOCLOSEPROCESS","SEE_MASK_NOQUERYCLASSSTORE","SEE_MASK_NOZONECHECKS","SEE_MASK_NO_CONSOLE","SEE_MASK_UNICODE","SEE_MASK_WAITFORINPUTIDLE","SE_ERR_ACCESSDENIED","SE_ERR_ASSOCINCOMPLETE","SE_ERR_DDEBUSY","SE_ERR_DDEFAIL","SE_ERR_DDETIMEOUT","SE_ERR_DLLNOTFOUND","SE_ERR_FNF","SE_ERR_NOASSOC","SE_ERR_OOM","SE_ERR_PNF","SE_ERR_SHARE","SHELLEXECUTEINFO","SHELLEXECUTEINFO structure [Windows Shell]","SHELLEXECUTEINFOW","_SHELLEXECUTEINFOA","_SHELLEXECUTEINFOW","_win32_SHELLEXECUTEINFO","edit","explore","find","open","print","properties","shell.SHELLEXECUTEINFO","shellapi/LPSHELLEXECUTEINFO","shellapi/SHELLEXECUTEINFO"]
old-location: shell\SHELLEXECUTEINFO.htm
tech.root: shell
ms.assetid: 50e0dac3-b5dc-4d9f-8fd7-3a53a428166b
ms.date: 12/05/2018
ms.keywords: '*LPSHELLEXECUTEINFOW, LPSHELLEXECUTEINFO, LPSHELLEXECUTEINFO structure pointer [Windows Shell], SEE_MASK_ASYNCOK, SEE_MASK_CLASSKEY, SEE_MASK_CLASSNAME, SEE_MASK_CONNECTNETDRV, SEE_MASK_DEFAULT, SEE_MASK_DOENVSUBST, SEE_MASK_FLAG_DDEWAIT, SEE_MASK_FLAG_HINST_IS_SITE, SEE_MASK_FLAG_LOG_USAGE, SEE_MASK_FLAG_NO_UI, SEE_MASK_HMONITOR, SEE_MASK_HOTKEY, SEE_MASK_ICON, SEE_MASK_IDLIST, SEE_MASK_INVOKEIDLIST, SEE_MASK_NOASYNC, SEE_MASK_NOCLOSEPROCESS, SEE_MASK_NOQUERYCLASSSTORE, SEE_MASK_NOZONECHECKS, SEE_MASK_NO_CONSOLE, SEE_MASK_UNICODE, SEE_MASK_WAITFORINPUTIDLE, SE_ERR_ACCESSDENIED, SE_ERR_ASSOCINCOMPLETE, SE_ERR_DDEBUSY, SE_ERR_DDEFAIL, SE_ERR_DDETIMEOUT, SE_ERR_DLLNOTFOUND, SE_ERR_FNF, SE_ERR_NOASSOC, SE_ERR_OOM, SE_ERR_PNF, SE_ERR_SHARE, SHELLEXECUTEINFO, SHELLEXECUTEINFO structure [Windows Shell], SHELLEXECUTEINFOW, _SHELLEXECUTEINFOA, _SHELLEXECUTEINFOW, _win32_SHELLEXECUTEINFO, edit, explore, find, open, print, properties, shell.SHELLEXECUTEINFO, shellapi/LPSHELLEXECUTEINFO, shellapi/SHELLEXECUTEINFO'
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: SHELLEXECUTEINFOW, *LPSHELLEXECUTEINFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _SHELLEXECUTEINFOW
 - shellapi/_SHELLEXECUTEINFOW
 - LPSHELLEXECUTEINFOW
 - shellapi/LPSHELLEXECUTEINFOW
 - SHELLEXECUTEINFOW
 - shellapi/SHELLEXECUTEINFOW
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Shellapi.h
api_name:
 - SHELLEXECUTEINFO - SHELLEXECUTEINFOW
no-loc: [verb, verbs, NULL, null, runas]
---

# SHELLEXECUTEINFOW structure

## -description

Contains information used by <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a>.

## -struct-fields

### -field cbSize

Type: <b>DWORD</b>

Required. The size of this structure, in bytes.

### -field fMask

Type: <b>ULONG</b>

A combination of one or more of the following values that indicate the content and validity of the other structure members:

<table>
<colgroup>
    <col span="1">
    <col span="1">
</colgroup>
<tr valign="top">
<td>SEE_MASK_DEFAULT (0x00000000)</td>
<td>Use default values.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_CLASSNAME (0x00000001)</td>
<td>Use the class name given by the <b>lpClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_CLASSKEY (0x00000003)
</td>
<td>Use the class key given by the <b>hkeyClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_IDLIST (0x00000004)</td>
<td>Use the item identifier list given by the <b>lpIDList</b> member. The <b>lpIDList</b> member must point to an <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_INVOKEIDLIST (0x0000000C)</td>
<td>Use the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a> interface of the selected item's <a href="/windows/desktop/shell/context-menu-handlers">shortcut menu handler</a>. Use either <b>lpFile</b> to identify the item by its file system path or <b>lpIDList</b> to identify the item by its PIDL. This flag allows applications to use <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> to invoke verbs from shortcut menu extensions instead of the static verbs listed in the registry.
<div class="alert"><b>Note:</b> SEE_MASK_INVOKEIDLIST overrides and implies SEE_MASK_IDLIST.</div>
<div> </div>
</td>
</tr>
<tr valign="top">
<td>SEE_MASK_ICON (0x00000010)</td>
<td>Use the icon given by the <b>hIcon</b> member. This flag cannot be combined with SEE_MASK_HMONITOR.
<div class="alert"><b>Note:</b> This flag is used only in Windows XP and earlier. It is ignored as of Windows Vista.</div>
</td>
</tr>
<tr valign="top">
<td>SEE_MASK_HOTKEY (0x00000020)</td>
<td>Use the keyboard shortcut given by the <b>dwHotKey</b> member.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_NOCLOSEPROCESS (0x00000040)</td>
<td>Use to indicate that the <b>hProcess</b> member receives the process handle. This handle is typically used to allow an application to find out when a process created with <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> terminates. In some cases, such as when execution is satisfied through a DDE conversation, no handle will be returned. The calling application is responsible for closing the handle when it is no longer needed.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_CONNECTNETDRV (0x00000080)</td>
<td>Validate the share and connect to a drive letter. This enables reconnection of disconnected network drives. The <b>lpFile</b> member is a UNC path of a file on a network.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_NOASYNC (0x00000100)</td>
<td>Only respected when launching files, does not apply to uris or shell namespace items (e.g. "This PC"). Wait for the async part of the execute operation, (e.g. DDE) to complete before returning. When this applies it ensures the launching operation finishes before returning. Applications that exit immediately after calling <b>ShellExecuteEx</b> should specify this flag. Note, <b>ShellExecuteEx</b> moves its work to a background thread if the caller's threading model is not Apartment. Forcing the call to be synchronous disables that behavior and uses the callers COM apartment. Specifing SEE_MASK_FLAG_HINST_IS_SITE forces synchronous behavior always.

If the execute operation is performed on a background thread and the caller did not specify the SEE_MASK_ASYNCOK flag, then the calling thread waits until the new process has started before returning. This typically means that either <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> has been called, the DDE communication has completed, or that the custom execution delegate has notified <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> that it is done. If the SEE_MASK_WAITFORINPUTIDLE flag is specified, then <b>ShellExecuteEx</b> calls <a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a> and waits for the new process to idle before returning, with a maximum timeout of 1 minute.

For further discussion on when this flag is necessary, see the Remarks section.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_FLAG_DDEWAIT (0x00000100)</td>
<td>The same as SEE_MASK_NOASYNC, use of that option is preferred.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_DOENVSUBST (0x00000200)</td>
<td>Expand any environment variables specified in the string given by the <b>lpDirectory</b> or <b>lpFile</b> member.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_FLAG_NO_UI (0x00000400)</td>
<td>Do not display user interface (UI) error dialogs that would normally be presented without this option. Security prompts are exempted and will still be shown.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_UNICODE (0x00004000)
</td>
<td>Use this flag to indicate a Unicode application.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_NO_CONSOLE (0x00008000)</td>
<td>Use to inherit the parent's console for the new process instead of having it create a new console. It is the opposite of using a CREATE_NEW_CONSOLE flag with <a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_ASYNCOK (0x00100000)
</td>
<td>The execution can be performed on a background thread and the call should return immediately without waiting for the background thread to finish. Note that in certain cases <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> ignores this flag and waits for the process to finish before returning.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_NOQUERYCLASSSTORE (0x01000000)</td>
<td>Not used.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_HMONITOR (0x00200000)</td>
<td>Use this flag when specifying a monitor on multi-monitor systems. The monitor is specified in the <b>hMonitor</b> member. This flag cannot be combined with SEE_MASK_ICON.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_NOZONECHECKS (0x00800000)</td>
<td>Do not perform a zone check. This flag allows <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> to bypass zone checking put into place by <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iattachmentexecute">IAttachmentExecute</a>.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_WAITFORINPUTIDLE (0x02000000)</td>
<td>After the new process is created, wait for the process to become idle before returning, with a one minute timeout. See <a href="/windows/desktop/api/winuser/nf-winuser-waitforinputidle">WaitForInputIdle</a> for more details.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_FLAG_LOG_USAGE (0x04000000)</td>
<td>Indicates a user initiated launch that enables tracking of frequently used programs and other behaviors.</td>
</tr>
<tr valign="top">
<td>SEE_MASK_FLAG_HINST_IS_SITE` (0x08000000)</td>
<td>The <b>hInstApp</b> member is used to specify the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> of an object that implements <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678965(v=vs.85)">IServiceProvider</a>. This object will be used as a site pointer. The site pointer is used to provide services to the <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> function, the handler binding process, and invoked verb handlers.
 
<a href="/windows/win32/api/shobjidl_core/nn-shobjidl_core-icreatingprocess">ICreatingProcess</a> can be provided to allow the caller to alter some parameters of the process being created.

This flag is supported in Windows 8 and later.

When this option is specified the call runs synchronously on the calling thread.
</td>
</tr>
</table>

### -field hwnd

Type: <b>HWND</b>

Optional. A handle to the owner window, used to display and position any UI that the system might produce while executing this function.

### -field lpVerb

Type: <b>LPCTSTR</b>

A string, referred to as a <i>verb</i>, that specifies the action to be performed. The set of available verbs depends on the particular file or folder. Generally, the actions available from an object's shortcut menu are available verbs. This parameter can be <b>NULL</b>, in which case the default verb is used if available. If not, the ":::no-loc text="open"::" verb is used. If neither verb is available, the system uses the first verb listed in the registry. The following verbs are commonly used:

- **:::no-loc text="edit":::**: Launches an editor and opens the document for editing. If <b>lpFile</b> is not a document file, the function will fail.
- **:::no-loc text="explore":::**: Explores the folder specified by <b>lpFile</b>.
- **:::no-loc text="find":::**: Initiates a search starting from the specified directory.
- **:::no-loc text="open":::**: Opens the file specified by the <b>lpFile</b> parameter. The file can be an executable file, a document file, or a folder.
- **:::no-loc text="openas":::**: Launches a picker UI allowing the user to select an app with which to open the file specified by the <b>lpFile</b> parameter. 
- **:::no-loc text="print":::**: Prints the document file specified by <b>lpFile</b>. If <b>lpFile</b> is not a document file, the function will fail.
- **:::no-loc text="properties":::**: Displays the file or folder's properties.
- **runas**: Launches an application as Administrator. User Account Control (UAC) will prompt the user for consent to run the application elevated or enter the credentials of an administrator account used to run the application.

### -field lpFile

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the name of the file or object on which <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> will perform the action specified by the <b>lpVerb</b> parameter. The system registry verbs that are supported by the <b>ShellExecuteEx</b> function include ":::no-loc text="open"::" for executable files and document files and ":::no-loc text="print"::" for document files for which a print handler has been registered. Other applications might have added Shell verbs through the system registry, such as ":::no-loc text="play"::" for .avi and .wav files. To specify a Shell namespace object, pass the fully qualified parse name and set the <b>SEE_MASK_INVOKEIDLIST</b> flag in the <b>fMask</b> parameter.

<div class="alert"><b>Note:</b> If the <b>SEE_MASK_INVOKEIDLIST</b> flag is set, you can use either <b>lpFile</b> or <b>lpIDList</b> to identify the item by its file system path or its PIDL respectively. One of the two values—<b>lpFile</b> or <b>lpIDList</b>—must be set.</div>

<div class="alert"><b>Note:</b> If the path is not included with the name, the current directory is assumed.</div>

### -field lpParameters

Type: <b>LPCTSTR</b>

Optional. The address of a null-terminated string that contains the application parameters. The parameters must be separated by spaces. If the <b>lpFile</b> member specifies a document file, <b>lpParameters</b> should be <b>NULL</b>.

### -field lpDirectory

Type: <b>LPCTSTR</b>

Optional. The address of a null-terminated string that specifies the name of the working directory. If this member is <b>NULL</b>, the current directory is used as the working directory.

### -field nShow

Type: <b>int</b>

Required. Flags that specify how an application is to be shown when it is opened; one of the SW_ values listed for the <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecutea">ShellExecute</a> function. If <b>lpFile</b> specifies a document file, the flag is simply passed to the associated application. It is up to the application to decide how to handle it.

### -field hInstApp

Type: <b>HINSTANCE</b>

[out] If SEE_MASK_NOCLOSEPROCESS is set and the <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> call succeeds, it sets this member to a value greater than 32. If the function fails, it is set to an SE_ERR_XXX error value that indicates the cause of the failure. Although <b>hInstApp</b> is declared as an HINSTANCE for compatibility with 16-bit Windows applications, it is not a true HINSTANCE. It can be cast only to an <b>int</b> and compared to either 32 or the following SE_ERR_XXX error codes.

<br/>

| Error Code | Reason |
| ---------- | ------ |
| SE_ERR_FNF (2) | File not found. |
| SE_ERR_PNF (3) | Path not found. |
| SE_ERR_ACCESSDENIED (5) | Access denied. |
| SE_ERR_OOM (8) | Out of memory. |
| SE_ERR_DLLNOTFOUND (32) | Dynamic-link library not found. |
| SE_ERR_SHARE (26) | Cannot share an open file. |
| SE_ERR_ASSOCINCOMPLETE (27) | File association information not complete. |
| SE_ERR_DDETIMEOUT (28) | DDE operation timed out. |
| SE_ERR_DDEFAIL (29) | DDE operation failed. |
| SE_ERR_DDEBUSY (30) | DDE operation is busy. |
| SE_ERR_NOASSOC (31) | File association not available. |

### -field lpIDList

Type: <b>LPVOID</b>

The address of an absolute <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> structure (PCIDLIST_ABSOLUTE) to contain an item identifier list that uniquely identifies the file to execute. This member is ignored if the <b>fMask</b> member does not include <b>SEE_MASK_IDLIST</b> or <b>SEE_MASK_INVOKEIDLIST</b>.

### -field lpClass

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies one of the following:

- A ProgId. For example, "Paint.Picture".</li>
- A URI protocol scheme. For example, "http".</li>
- A file extension. For example, ".txt".</li>
- A registry path under HKEY_CLASSES_ROOT that names a subkey that contains one or more Shell verbs. This key will have a subkey that conforms to the Shell verb registry schema, such as <b>shell</b>&#92;<i>verb name</i>.

This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_CLASSNAME</b>.

### -field hkeyClass

Type: <b>HKEY</b>

A handle to the registry key for the file type. The access rights for this registry key should be set to KEY_READ. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_CLASSKEY</b>.

### -field dwHotKey

Type: <b>DWORD</b>

A keyboard shortcut to associate with the application. The low-order word is the virtual key code, and the high-order word is a modifier flag (HOTKEYF_). For a list of modifier flags, see the description of the <a href="/windows/desktop/inputdev/wm-sethotkey">WM_SETHOTKEY</a> message. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_HOTKEY</b>.

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.hIcon

Type: <b>HANDLE</b>

A handle to the icon for the file type. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_ICON</b>. This value is used only in Windows XP and earlier. It is ignored as of Windows Vista.

### -field DUMMYUNIONNAME.hMonitor

Type: <b>HANDLE</b>

A handle to the monitor upon which the document is to be displayed. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_HMONITOR</b>.

### -field hProcess

Type: <b>HANDLE</b>

A handle to the newly started application. This member is set on return and is always <b>NULL</b> unless <b>fMask</b> is set to <b>SEE_MASK_NOCLOSEPROCESS</b>. Even if <b>fMask</b> is set to <b>SEE_MASK_NOCLOSEPROCESS</b>, <b>hProcess</b> will be <b>NULL</b> if no process was launched. For example, if a document to be launched is a URL and an instance of Internet Explorer is already running, it will display the document. No new process is launched, and <b>hProcess</b> will be <b>NULL</b>.

<div class="alert"><b>Note:</b> <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> does not always return an <b>hProcess</b>, even if a process is launched as the result of the call. For example, an <b>hProcess</b> does not return when you use <b>SEE_MASK_INVOKEIDLIST</b> to invoke <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icontextmenu">IContextMenu</a>.</div>

## -remarks

The <b>SEE_MASK_NOASYNC</b> flag must be specified if the thread calling <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> does not have a message loop or if the thread or process will terminate soon after <b>ShellExecuteEx</b> returns. Under such conditions, the calling thread will not be available to complete the DDE conversation, so it is important that <b>ShellExecuteEx</b> complete the conversation before returning control to the calling application. Failure to complete the conversation can result in an unsuccessful launch of the document.

If the calling thread has a message loop and will exist for some time after the call to <a href="/windows/desktop/api/shellapi/nf-shellapi-shellexecuteexa">ShellExecuteEx</a> returns, the <b>SEE_MASK_NOASYNC</b> flag is optional. If the flag is omitted, the calling thread's message pump will be used to complete the DDE conversation. The calling application regains control sooner, since the DDE conversation can be completed in the background.

For calls to this API that result from user interaction specify <b>SEE_MASK_FLAG_LOG_USAGE</b>.

To include double quotation marks in <b>lpParameters</b>, enclose each mark in a pair of quotation marks, as in the following example.

``` cpp
sei.lpParameters = "An example: \"\"\"quoted text\"\"\"";
```

In this case, the application receives three parameters: <i>An</i>, <i>example:</i>, and <i>"quoted text"</i>.

> [!NOTE]
> The shellapi.h header defines SHELLEXECUTEINFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).
