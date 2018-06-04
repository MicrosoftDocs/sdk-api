---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _SHELLEXECUTEINFOW structure


## -description


Contains information used by <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

Required. The size of this structure, in bytes.


### -field fMask

Type: <b>ULONG</b>

Flags that indicate the content and validity of the other structure members; a combination of the following values:



#### SEE_MASK_DEFAULT (0x00000000)

Use default values.



#### SEE_MASK_CLASSNAME (0x00000001)

Use the class name given by the <b>lpClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.



#### SEE_MASK_CLASSKEY (0x00000003)

Use the class key given by the <b>hkeyClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.



#### SEE_MASK_IDLIST (0x00000004)

Use the item identifier list given by the <b>lpIDList</b> member. The <b>lpIDList</b> member must point to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.



#### SEE_MASK_INVOKEIDLIST (0x0000000C)

Use the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface of the selected item's <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">shortcut menu handler</a>. Use either <b>lpFile</b> to identify the item by its file system path or <b>lpIDList</b> to identify the item by its PIDL. This flag allows applications to use <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> to invoke verbs from shortcut menu extensions instead of the static verbs listed in the registry.

<div class="alert"><b>Note</b>  SEE_MASK_INVOKEIDLIST overrides and implies SEE_MASK_IDLIST.</div>
<div> </div>


#### SEE_MASK_ICON (0x00000010)

Use the icon given by the <b>hIcon</b> member. This flag cannot be combined with SEE_MASK_HMONITOR.
                                
                                

<div class="alert"><b>Note</b>  This flag is used only in Windows XP and earlier. It is ignored as of Windows Vista.</div>
<div> </div>


#### SEE_MASK_HOTKEY (0x00000020)

Use the keyboard shortcut given by the <b>dwHotKey</b> member.



#### SEE_MASK_NOCLOSEPROCESS (0x00000040)

Use to indicate that the <b>hProcess</b> member receives the process handle. This handle is typically used to allow an application to find out when a process created with <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> terminates. In some cases, such as when execution is satisfied through a DDE conversation, no handle will be returned. The calling application is responsible for closing the handle when it is no longer needed.



#### SEE_MASK_CONNECTNETDRV (0x00000080)

Validate the share and connect to a drive letter. This enables reconnection of disconnected network drives. The <b>lpFile</b> member is a UNC path of a file on a network.



#### SEE_MASK_NOASYNC (0x00000100)

Wait for the execute operation to complete before returning. This flag should be used by callers that are using ShellExecute forms that might result in an async activation, for example DDE, and create a process that might be run on a background thread. (Note: <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> runs on a background thread by default if the caller's threading model is not Apartment.) Calls to <b>ShellExecuteEx</b> from processes already running on background threads should always pass this flag. Also, applications that exit immediately after calling <b>ShellExecuteEx</b> should specify this flag.

If the execute operation is performed on a background thread and the caller did not specify the SEE_MASK_ASYNCOK flag, then the calling thread waits until the new process has started before returning. This typically means that either <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> has been called, the DDE communication has completed, or that the custom execution delegate has notified <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> that it is done. If the SEE_MASK_WAITFORINPUTIDLE flag is specified, then <b>ShellExecuteEx</b> calls <a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> and waits for the new process to idle before returning, with a maximum timeout of 1 minute.

For further discussion on when this flag is necessary, see the Remarks section.



#### SEE_MASK_FLAG_DDEWAIT (0x00000100)

Do not use; use SEE_MASK_NOASYNC instead.



#### SEE_MASK_DOENVSUBST (0x00000200)

Expand any environment variables specified in the string given by the <b>lpDirectory</b> or <b>lpFile</b> member.



#### SEE_MASK_FLAG_NO_UI (0x00000400)

Do not display an error message box if an error occurs.



#### SEE_MASK_UNICODE (0x00004000)

Use this flag to indicate a Unicode application.



#### SEE_MASK_NO_CONSOLE (0x00008000)

Use to inherit the parent's console for the new process instead of having it create a new console. It is the opposite of using a CREATE_NEW_CONSOLE flag with <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.



#### SEE_MASK_ASYNCOK (0x00100000)

The execution can be performed on a background thread and the call should return immediately without waiting for the background thread to finish. Note that in certain cases <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> ignores this flag and waits for the process to finish before returning.



#### SEE_MASK_NOQUERYCLASSSTORE (0x01000000)

Not used.



#### SEE_MASK_HMONITOR (0x00200000)

Use this flag when specifying a monitor on multi-monitor systems. The monitor is specified in the <b>hMonitor</b> member. This flag cannot be combined with SEE_MASK_ICON.



#### SEE_MASK_NOZONECHECKS (0x00800000)

<b>Introduced in Windows XP</b>. Do not perform a zone check. This flag allows <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> to bypass zone checking put into place by <a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>.



#### SEE_MASK_WAITFORINPUTIDLE (0x02000000)

After the new process is created, wait for the process to become idle before returning, with a one minute timeout. See <a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> for more details.



#### SEE_MASK_FLAG_LOG_USAGE (0x04000000)

<b>Introduced in Windows XP</b>. Keep track of the number of times this application has been launched. Applications with sufficiently high counts appear in the Start Menu's list of most frequently used programs.



#### SEE_MASK_FLAG_HINST_IS_SITE (0x08000000)

The <b>hInstApp</b> member is used to specify the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of an object that implements <a href="_inet_iserviceprovider_interface">IServiceProvider</a>. This object will be used as a site pointer. The site pointer is used to provide services to the <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> function, the handler binding process, and invoked verb handlers.

To use <b>SEE_MASK_FLAG_HINST_IS_SITE</b> in operating systems prior to Windows 8, define it manually in your program: #define SEE_MASK_FLAG_HINST_IS_SITE 0x08000000.


### -field hwnd

Type: <b>HWND</b>

Optional. A handle to the parent window, used to display any message boxes that the system might produce while executing this function. This value can be <b>NULL</b>.


### -field lpVerb

Type: <b>LPCTSTR</b>

A string, referred to as a <i>verb</i>, that specifies the action to be performed. The set of available verbs depends on the particular file or folder. Generally, the actions available from an object's shortcut menu are available verbs. This parameter can be <b>NULL</b>, in which case the default verb is used if available. If not, the "open" verb is used. If neither verb is available, the system uses the first verb listed in the registry. The following verbs are commonly used:
                        
                        



#### edit

Launches an editor and opens the document for editing. If <b>lpFile</b> is not a document file, the function will fail.



#### explore

Explores the folder specified by <b>lpFile</b>.



#### find

Initiates a search starting from the specified directory.



#### open

Opens the file specified by the <b>lpFile</b> parameter. The file can be an executable file, a document file, or a folder.



#### print

Prints the document file specified by <b>lpFile</b>. If <b>lpFile</b> is not a document file, the function will fail.



#### properties

Displays the file or folder's properties.


### -field lpFile

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies the name of the file or object on which <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> will perform the action specified by the <b>lpVerb</b> parameter. The system registry verbs that are supported by the <b>ShellExecuteEx</b> function include "open" for executable files and document files and "print" for document files for which a print handler has been registered. Other applications might have added Shell verbs through the system registry, such as "play" for .avi and .wav files. To specify a Shell namespace object, pass the fully qualified parse name and set the <b>SEE_MASK_INVOKEIDLIST</b> flag in the <b>fMask</b> parameter.

<div class="alert"><b>Note</b>  If the <b>SEE_MASK_INVOKEIDLIST</b> flag is set, you can use either <b>lpFile</b> or <b>lpIDList</b> to identify the item by its file system path or its PIDL respectively. One of the two values—<b>lpFile</b> or <b>lpIDList</b>—must be set.</div>
<div> </div>
<div class="alert"><b>Note</b>  If the path is not included with the name, the current directory is assumed.</div>
<div> </div>

### -field lpParameters

Type: <b>LPCTSTR</b>

Optional. The address of a null-terminated string that contains the application parameters. The parameters must be separated by spaces. If the <b>lpFile</b> member specifies a document file, <b>lpParameters</b> should be <b>NULL</b>.


### -field lpDirectory

Type: <b>LPCTSTR</b>

Optional. The address of a null-terminated string that specifies the name of the working directory. If this member is <b>NULL</b>, the current directory is used as the working directory.


### -field nShow

Type: <b>int</b>

Required. Flags that specify how an application is to be shown when it is opened; one of the SW_ values listed for the <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> function. If <b>lpFile</b> specifies a document file, the flag is simply passed to the associated application. It is up to the application to decide how to handle it.


### -field hInstApp

Type: <b>HINSTANCE</b>

[out] If SEE_MASK_NOCLOSEPROCESS is set and the <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> call succeeds, it sets this member to a value greater than 32. If the function fails, it is set to an SE_ERR_XXX error value that indicates the cause of the failure. Although <b>hInstApp</b> is declared as an HINSTANCE for compatibility with 16-bit Windows applications, it is not a true HINSTANCE. It can be cast only to an <b>int</b> and compared to either 32 or the following SE_ERR_XXX error codes.



#### SE_ERR_FNF (2)

File not found.



#### SE_ERR_PNF (3)

Path not found.



#### SE_ERR_ACCESSDENIED (5)

Access denied.



#### SE_ERR_OOM (8)

Out of memory.



#### SE_ERR_DLLNOTFOUND (32)

Dynamic-link library not found.



#### SE_ERR_SHARE (26)

Cannot share an open file.



#### SE_ERR_ASSOCINCOMPLETE (27)

File association information not complete.



#### SE_ERR_DDETIMEOUT (28)

DDE operation timed out.



#### SE_ERR_DDEFAIL (29)

DDE operation failed.



#### SE_ERR_DDEBUSY (30)

DDE operation is busy.



#### SE_ERR_NOASSOC (31)

File association not available.


### -field lpIDList

Type: <b>LPVOID</b>

The address of an absolute <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure (PCIDLIST_ABSOLUTE) to contain an item identifier list that uniquely identifies the file to execute. This member is ignored if the <b>fMask</b> member does not include <b>SEE_MASK_IDLIST</b> or <b>SEE_MASK_INVOKEIDLIST</b>.


### -field lpClass

Type: <b>LPCTSTR</b>

The address of a null-terminated string that specifies one of the following:
                    
                        

<ul>
<li>A ProgId. For example, "Paint.Picture".</li>
<li>A URI protocol scheme. For example, "http".</li>
<li>A file extension. For example, ".txt".</li>
<li>A registry path under HKEY_CLASSES_ROOT that names a subkey that contains one or more Shell verbs. This key will have a subkey that conforms to the Shell verb registry schema, such as <b>shell</b>\<i>verb name</i></p>.</li>
</ul>


                        This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_CLASSNAME</b>.
                    


### -field hkeyClass

Type: <b>HKEY</b>

A handle to the registry key for the file type. The access rights for this registry key should be set to KEY_READ. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_CLASSKEY</b>.


### -field dwHotKey

Type: <b>DWORD</b>

A keyboard shortcut to associate with the application. The low-order word is the virtual key code, and the high-order word is a modifier flag (HOTKEYF_). For a list of modifier flags, see the description of the <a href="https://msdn.microsoft.com/b2c7e6ca-da71-440b-a05e-17f2da419d18">WM_SETHOTKEY</a> message. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_HOTKEY</b>.


### -field DUMMYUNIONNAME


### -field DUMMYUNIONNAME.hIcon

<b>Type: <b>HANDLE</b>
</b>
A handle to the icon for the file type. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_ICON</b>. This value is used only in Windows XP and earlier. It is ignored as of Windows Vista.


### -field DUMMYUNIONNAME.hMonitor

<b>Type: <b>HANDLE</b>
</b>
A handle to the monitor upon which the document is to be displayed. This member is ignored if <b>fMask</b> does not include <b>SEE_MASK_HMONITOR</b>.


### -field hProcess

Type: <b>HANDLE</b>

A handle to the newly started application. This member is set on return and is always <b>NULL</b> unless <b>fMask</b> is set to <b>SEE_MASK_NOCLOSEPROCESS</b>. Even if <b>fMask</b> is set to <b>SEE_MASK_NOCLOSEPROCESS</b>, <b>hProcess</b> will be <b>NULL</b> if no process was launched. For example, if a document to be launched is a URL and an instance of Internet Explorer is already running, it will display the document. No new process is launched, and <b>hProcess</b> will be <b>NULL</b>.

<div class="alert"><b>Note</b>  <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> does not always return an <b>hProcess</b>, even if a process is launched as the result of the call. For example, an <b>hProcess</b> does not return when you use <b>SEE_MASK_INVOKEIDLIST</b> to invoke <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a>.</div>
<div> </div>

##### - fMask.SEE_MASK_ASYNCOK (0x00100000)

The execution can be performed on a background thread and the call should return immediately without waiting for the background thread to finish. Note that in certain cases <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> ignores this flag and waits for the process to finish before returning.


##### - fMask.SEE_MASK_CLASSKEY (0x00000003)

Use the class key given by the <b>hkeyClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.


##### - fMask.SEE_MASK_CLASSNAME (0x00000001)

Use the class name given by the <b>lpClass</b> member. If both SEE_MASK_CLASSKEY and SEE_MASK_CLASSNAME are set, the class key is used.


##### - fMask.SEE_MASK_CONNECTNETDRV (0x00000080)

Validate the share and connect to a drive letter. This enables reconnection of disconnected network drives. The <b>lpFile</b> member is a UNC path of a file on a network.


##### - fMask.SEE_MASK_DEFAULT (0x00000000)

Use default values.


##### - fMask.SEE_MASK_DOENVSUBST (0x00000200)

Expand any environment variables specified in the string given by the <b>lpDirectory</b> or <b>lpFile</b> member.


##### - fMask.SEE_MASK_FLAG_DDEWAIT (0x00000100)

Do not use; use SEE_MASK_NOASYNC instead.


##### - fMask.SEE_MASK_FLAG_HINST_IS_SITE (0x08000000)

The <b>hInstApp</b> member is used to specify the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> of an object that implements <a href="_inet_iserviceprovider_interface">IServiceProvider</a>. This object will be used as a site pointer. The site pointer is used to provide services to the <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a> function, the handler binding process, and invoked verb handlers.

To use <b>SEE_MASK_FLAG_HINST_IS_SITE</b> in operating systems prior to Windows 8, define it manually in your program: #define SEE_MASK_FLAG_HINST_IS_SITE 0x08000000.


##### - fMask.SEE_MASK_FLAG_LOG_USAGE (0x04000000)

<b>Introduced in Windows XP</b>. Keep track of the number of times this application has been launched. Applications with sufficiently high counts appear in the Start Menu's list of most frequently used programs.


##### - fMask.SEE_MASK_FLAG_NO_UI (0x00000400)

Do not display an error message box if an error occurs.


##### - fMask.SEE_MASK_HMONITOR (0x00200000)

Use this flag when specifying a monitor on multi-monitor systems. The monitor is specified in the <b>hMonitor</b> member. This flag cannot be combined with SEE_MASK_ICON.


##### - fMask.SEE_MASK_HOTKEY (0x00000020)

Use the keyboard shortcut given by the <b>dwHotKey</b> member.


##### - fMask.SEE_MASK_ICON (0x00000010)

Use the icon given by the <b>hIcon</b> member. This flag cannot be combined with SEE_MASK_HMONITOR.
                                
                                

<div class="alert"><b>Note</b>  This flag is used only in Windows XP and earlier. It is ignored as of Windows Vista.</div>
<div> </div>

##### - fMask.SEE_MASK_IDLIST (0x00000004)

Use the item identifier list given by the <b>lpIDList</b> member. The <b>lpIDList</b> member must point to an <a href="https://msdn.microsoft.com/60daf071-4e93-4e1c-bc38-894f706db04f">ITEMIDLIST</a> structure.


##### - fMask.SEE_MASK_INVOKEIDLIST (0x0000000C)

Use the <a href="https://msdn.microsoft.com/6ea0b8f9-4a05-4a4b-adc5-d540eb3287ee">IContextMenu</a> interface of the selected item's <a href="https://msdn.microsoft.com/cff79cdc-8a01-4575-9af7-2a485c6a8e46">shortcut menu handler</a>. Use either <b>lpFile</b> to identify the item by its file system path or <b>lpIDList</b> to identify the item by its PIDL. This flag allows applications to use <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> to invoke verbs from shortcut menu extensions instead of the static verbs listed in the registry.

<div class="alert"><b>Note</b>  SEE_MASK_INVOKEIDLIST overrides and implies SEE_MASK_IDLIST.</div>
<div> </div>

##### - fMask.SEE_MASK_NOASYNC (0x00000100)

Wait for the execute operation to complete before returning. This flag should be used by callers that are using ShellExecute forms that might result in an async activation, for example DDE, and create a process that might be run on a background thread. (Note: <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> runs on a background thread by default if the caller's threading model is not Apartment.) Calls to <b>ShellExecuteEx</b> from processes already running on background threads should always pass this flag. Also, applications that exit immediately after calling <b>ShellExecuteEx</b> should specify this flag.

If the execute operation is performed on a background thread and the caller did not specify the SEE_MASK_ASYNCOK flag, then the calling thread waits until the new process has started before returning. This typically means that either <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a> has been called, the DDE communication has completed, or that the custom execution delegate has notified <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> that it is done. If the SEE_MASK_WAITFORINPUTIDLE flag is specified, then <b>ShellExecuteEx</b> calls <a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> and waits for the new process to idle before returning, with a maximum timeout of 1 minute.

For further discussion on when this flag is necessary, see the Remarks section.


##### - fMask.SEE_MASK_NOCLOSEPROCESS (0x00000040)

Use to indicate that the <b>hProcess</b> member receives the process handle. This handle is typically used to allow an application to find out when a process created with <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> terminates. In some cases, such as when execution is satisfied through a DDE conversation, no handle will be returned. The calling application is responsible for closing the handle when it is no longer needed.


##### - fMask.SEE_MASK_NOQUERYCLASSSTORE (0x01000000)

Not used.


##### - fMask.SEE_MASK_NOZONECHECKS (0x00800000)

<b>Introduced in Windows XP</b>. Do not perform a zone check. This flag allows <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> to bypass zone checking put into place by <a href="https://msdn.microsoft.com/2ebc3197-aa28-446e-8452-8ff71764fa9d">IAttachmentExecute</a>.


##### - fMask.SEE_MASK_NO_CONSOLE (0x00008000)

Use to inherit the parent's console for the new process instead of having it create a new console. It is the opposite of using a CREATE_NEW_CONSOLE flag with <a href="https://msdn.microsoft.com/library/windows/hardware/ff539321">CreateProcess</a>.


##### - fMask.SEE_MASK_UNICODE (0x00004000)

Use this flag to indicate a Unicode application.


##### - fMask.SEE_MASK_WAITFORINPUTIDLE (0x02000000)

After the new process is created, wait for the process to become idle before returning, with a one minute timeout. See <a href="https://msdn.microsoft.com/2a684921-36f1-438c-895c-5bebc242635a">WaitForInputIdle</a> for more details.


##### - hInstApp.SE_ERR_ACCESSDENIED (5)

Access denied.


##### - hInstApp.SE_ERR_ASSOCINCOMPLETE (27)

File association information not complete.


##### - hInstApp.SE_ERR_DDEBUSY (30)

DDE operation is busy.


##### - hInstApp.SE_ERR_DDEFAIL (29)

DDE operation failed.


##### - hInstApp.SE_ERR_DDETIMEOUT (28)

DDE operation timed out.


##### - hInstApp.SE_ERR_DLLNOTFOUND (32)

Dynamic-link library not found.


##### - hInstApp.SE_ERR_FNF (2)

File not found.


##### - hInstApp.SE_ERR_NOASSOC (31)

File association not available.


##### - hInstApp.SE_ERR_OOM (8)

Out of memory.


##### - hInstApp.SE_ERR_PNF (3)

Path not found.


##### - hInstApp.SE_ERR_SHARE (26)

Cannot share an open file.


##### - lpVerb.edit

Launches an editor and opens the document for editing. If <b>lpFile</b> is not a document file, the function will fail.


##### - lpVerb.explore

Explores the folder specified by <b>lpFile</b>.


##### - lpVerb.find

Initiates a search starting from the specified directory.


##### - lpVerb.open

Opens the file specified by the <b>lpFile</b> parameter. The file can be an executable file, a document file, or a folder.


##### - lpVerb.print

Prints the document file specified by <b>lpFile</b>. If <b>lpFile</b> is not a document file, the function will fail.


##### - lpVerb.properties

Displays the file or folder's properties.


## -remarks



The <b>SEE_MASK_NOASYNC</b> flag must be specified if the thread calling <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> does not have a message loop or if the thread or process will terminate soon after <b>ShellExecuteEx</b> returns. Under such conditions, the calling thread will not be available to complete the DDE conversation, so it is important that <b>ShellExecuteEx</b> complete the conversation before returning control to the calling application. Failure to complete the conversation can result in an unsuccessful launch of the document.

If the calling thread has a message loop and will exist for some time after the call to <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a> returns, the <b>SEE_MASK_NOASYNC</b> flag is optional. If the flag is omitted, the calling thread's message pump will be used to complete the DDE conversation. The calling application regains control sooner, since the DDE conversation can be completed in the background.

When populating the most frequently used program list using the <b>SEE_MASK_FLAG_LOG_USAGE</b> flag in <b>fMask</b>, counts are made differently for the classic and Windows XP-style Start menus. The classic style menu only counts hits to the shortcuts in the Program menu. The Windows XP-style menu counts both hits to the shortcuts in the Program menu and hits to those shortcuts' targets outside of the Program menu. Therefore, setting <b>lpFile</b> to myfile.exe would affect the count for the Windows XP-style menu regardless of whether that file was launched directly or through a shortcut. The classic style—which would require <b>lpFile</b> to contain a .lnk file name—would not be affected.

To include double quotation marks in <b>lpParameters</b>, enclose each mark in a pair of quotation marks, as in the following example. 

                

<pre class="syntax" xml:space="preserve"><code>sei.lpParameters = "An example: \"\"\"quoted text\"\"\"";</code></pre>


                In this case, the application receives three parameters: <i>An</i>, <i>example:</i>, and <i>"quoted text"</i>.



