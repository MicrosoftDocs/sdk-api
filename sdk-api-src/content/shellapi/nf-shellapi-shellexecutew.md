---
UID: NF:shellapi.ShellExecuteW
title: ShellExecuteW function
author: windows-sdk-content
description: Performs an operation on a specified file.
old-location: shell\ShellExecute.htm
tech.root: shell
ms.assetid: 8b1f3978-a0ee-4684-8a37-98e270b63897
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: NULL, SW_HIDE, SW_MAXIMIZE, SW_MINIMIZE, SW_RESTORE, SW_SHOW, SW_SHOWDEFAULT, SW_SHOWMAXIMIZED, SW_SHOWMINIMIZED, SW_SHOWMINNOACTIVE, SW_SHOWNA, SW_SHOWNOACTIVATE, SW_SHOWNORMAL, ShellExecute, ShellExecute function [Windows Shell], ShellExecuteA, ShellExecuteW, _win32_ShellExecute, _win32_ShellExecute_cpp, edit, explore, find, open, print, shell.ShellExecute, shellapi/ShellExecute, shellapi/ShellExecuteA, shellapi/ShellExecuteW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: shellapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: ShellExecuteW (Unicode) and ShellExecuteA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Shell32.lib
req.dll: Shell32.dll (version 3.51 or later)
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Shell32.dll
 - Ext-MS-Win-shell-shell32-l1-2-0.dll
 - ext-ms-win-shell-shell32-l1-1-0.dll
 - ext-ms-win-shell-shell32-l1-2-1.dll
 - Ext-MS-Win-Shell-Shell32-L1-2-2.dll
api_name:
 - ShellExecute
 - ShellExecuteA
 - ShellExecuteW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ShellExecuteW function


## -description


Performs an operation on a specified file.


## -parameters




### -param hwnd [in, optional]

Type: <b>HWND</b>

A handle to the parent window used for displaying a UI or error messages. This value can be <b>NULL</b> if the operation is not associated with a window.


### -param lpOperation [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string, referred to in this case as a <i>verb</i>, that specifies the action to be performed. The set of available verbs depends on the particular file or folder. Generally, the actions available from an object's shortcut menu are available verbs. The following verbs are commonly used:



#### edit

Launches an editor and opens the document for editing. If <i>lpFile</i> is not a document file, the function will fail.



#### explore

Explores a folder specified by <i>lpFile</i>.



#### find

Initiates a search beginning in the directory specified by <i>lpDirectory</i>.



#### open

Opens the item specified by the <i>lpFile</i> parameter. The item can be a file or folder.



#### print

Prints the file specified by <i>lpFile</i>. If <i>lpFile</i> is not a document file, the function fails.



#### NULL

The default verb is used, if available. If not, the "open" verb is used. If neither verb is available, the system uses the first verb listed in the registry.


### -param lpFile [in]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string that specifies the file or object on which to execute the specified verb. To specify a Shell namespace object, pass the fully qualified parse name. Note that not all verbs are supported on all objects. For example, not all document types support the "print" verb. If a relative path is used for the <i>lpDirectory</i> parameter do not use a relative path for <i>lpFile</i>.


### -param lpParameters [in, optional]

Type: <b>LPCTSTR</b>

If <i>lpFile</i> specifies an executable file, this parameter is a pointer to a <b>null</b>-terminated string that specifies the parameters to be passed to the application. The format of this string is determined by the verb that is to be invoked. If <i>lpFile</i> specifies a document file, <i>lpParameters</i> should be <b>NULL</b>.


### -param lpDirectory [in, optional]

Type: <b>LPCTSTR</b>

A pointer to a <b>null</b>-terminated string that specifies the default (working) directory for the action. If this value is <b>NULL</b>, the current working directory is used. If a relative path is provided at <i>lpFile</i>, do not use a relative path for <i>lpDirectory</i>.


### -param nShowCmd [in]

Type: <b>INT</b>

The flags that specify how an application is to be displayed when it is opened. If <i>lpFile</i> specifies a document file, the flag is simply passed to the associated application. It is up to the application to decide how to handle it. These values are defined in Winuser.h.



#### SW_HIDE (0)

Hides the window and activates another window.



#### SW_MAXIMIZE (3)

Maximizes the specified window.



#### SW_MINIMIZE (6)

Minimizes the specified window and activates the next top-level window in the z-order.



#### SW_RESTORE (9)

Activates and displays the window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when restoring a minimized window.



#### SW_SHOW (5)

Activates the window and displays it in its current size and position.



#### SW_SHOWDEFAULT (10)

Sets the show state based on the SW_ flag specified in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function by the program that started the application. An application should call <a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a> with this flag to set the initial show state of its main window.



#### SW_SHOWMAXIMIZED (3)

Activates the window and displays it as a maximized window.



#### SW_SHOWMINIMIZED (2)

Activates the window and displays it as a minimized window.



#### SW_SHOWMINNOACTIVE (7)

Displays the window as a minimized window. The active window remains active.



#### SW_SHOWNA (8)

Displays the window in its current state. The active window remains active.



#### SW_SHOWNOACTIVATE (4)

Displays a window in its most recent size and position. The active window remains active.



#### SW_SHOWNORMAL (1)

Activates and displays a window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when displaying the window for the first time.


##### - lpOperation.NULL

The default verb is used, if available. If not, the "open" verb is used. If neither verb is available, the system uses the first verb listed in the registry.


##### - lpOperation.edit

Launches an editor and opens the document for editing. If <i>lpFile</i> is not a document file, the function will fail.


##### - lpOperation.explore

Explores a folder specified by <i>lpFile</i>.


##### - lpOperation.find

Initiates a search beginning in the directory specified by <i>lpDirectory</i>.


##### - lpOperation.open

Opens the item specified by the <i>lpFile</i> parameter. The item can be a file or folder.


##### - lpOperation.print

Prints the file specified by <i>lpFile</i>. If <i>lpFile</i> is not a document file, the function fails.


##### - nShowCmd.SW_HIDE (0)

Hides the window and activates another window.


##### - nShowCmd.SW_MAXIMIZE (3)

Maximizes the specified window.


##### - nShowCmd.SW_MINIMIZE (6)

Minimizes the specified window and activates the next top-level window in the z-order.


##### - nShowCmd.SW_RESTORE (9)

Activates and displays the window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when restoring a minimized window.


##### - nShowCmd.SW_SHOW (5)

Activates the window and displays it in its current size and position.


##### - nShowCmd.SW_SHOWDEFAULT (10)

Sets the show state based on the SW_ flag specified in the <a href="https://msdn.microsoft.com/cf4b795c-52c1-4573-8328-99ee13f68bb3">STARTUPINFO</a> structure passed to the <a href="https://msdn.microsoft.com/3ef0a5b2-4d71-4c17-8188-76a4025287fc">CreateProcess</a> function by the program that started the application. An application should call <a href="https://msdn.microsoft.com/en-us/library/ms633548(v=VS.85).aspx">ShowWindow</a> with this flag to set the initial show state of its main window.


##### - nShowCmd.SW_SHOWMAXIMIZED (3)

Activates the window and displays it as a maximized window.


##### - nShowCmd.SW_SHOWMINIMIZED (2)

Activates the window and displays it as a minimized window.


##### - nShowCmd.SW_SHOWMINNOACTIVE (7)

Displays the window as a minimized window. The active window remains active.


##### - nShowCmd.SW_SHOWNA (8)

Displays the window in its current state. The active window remains active.


##### - nShowCmd.SW_SHOWNOACTIVATE (4)

Displays a window in its most recent size and position. The active window remains active.


##### - nShowCmd.SW_SHOWNORMAL (1)

Activates and displays a window. If the window is minimized or maximized, Windows restores it to its original size and position. An application should specify this flag when displaying the window for the first time.


## -returns



Type: <b>HINSTANCE</b>

If the function succeeds, it returns a value greater than 32. If the function fails, it returns an error value that indicates the cause of the failure. The return value is cast as an HINSTANCE for backward compatibility with 16-bit Windows applications. It is not a true HINSTANCE, however. It can be cast only to an <b>int</b> and compared to either 32 or the following error codes below.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
The operating system is out of memory or resources.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_FILE_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_PATH_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified path was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_BAD_FORMAT</b></dt>
</dl>
</td>
<td width="60%">
The .exe file is invalid (non-Win32 .exe or error in .exe image).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
The operating system denied access to the specified file.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_ASSOCINCOMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The file name association is incomplete or invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_DDEBUSY</b></dt>
</dl>
</td>
<td width="60%">
The DDE transaction could not be completed because other DDE transactions were being processed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_DDEFAIL</b></dt>
</dl>
</td>
<td width="60%">
The DDE transaction failed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_DDETIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The DDE transaction could not be completed because the request timed out.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_DLLNOTFOUND</b></dt>
</dl>
</td>
<td width="60%">
The specified DLL was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_FNF</b></dt>
</dl>
</td>
<td width="60%">
The specified file was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_NOASSOC</b></dt>
</dl>
</td>
<td width="60%">
There is no application associated with the given file name extension. This error will also be returned if you attempt to print a file that is not printable.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_OOM</b></dt>
</dl>
</td>
<td width="60%">
There was not enough memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_PNF</b></dt>
</dl>
</td>
<td width="60%">
The specified path was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>SE_ERR_SHARE</b></dt>
</dl>
</td>
<td width="60%">
A sharing violation occurred.

</td>
</tr>
</table>
 




## -remarks



Because <b>ShellExecute</b> can delegate execution to Shell extensions (data sources, context menu handlers, verb implementations) that are activated using Component Object Model (COM), COM should be initialized before <b>ShellExecute</b> is called. Some Shell extensions require the COM single-threaded apartment (STA) type. In that case, COM should be initialized as shown here:

                


```
CoInitializeEx(NULL, COINIT_APARTMENTTHREADED | COINIT_DISABLE_OLE1DDE)
```


There are certainly instances where <b>ShellExecute</b> does not use one of these types of Shell extension and those instances would not require COM to be initialized at all. Nonetheless, it is good practice to <i>always</i> initalize COM before using this function.

This method allows you to execute any commands in a folder's shortcut menu or stored in the registry.

To open a folder, use either of the following calls: 			

				


```
ShellExecute(handle, NULL, <fully_qualified_path_to_folder>, NULL, NULL, SW_SHOWNORMAL);
```


or


```
ShellExecute(handle, "open", <fully_qualified_path_to_folder>, NULL, NULL, SW_SHOWNORMAL);
```


To explore a folder, use the following call:
				


```
ShellExecute(handle, "explore", <fully_qualified_path_to_folder>, NULL, NULL, SW_SHOWNORMAL);
```


To launch the Shell's Find utility for a directory, use the following call.
				


```
ShellExecute(handle, "find", <fully_qualified_path_to_folder>, NULL, NULL, 0);
```


If <i>lpOperation</i> is <b>NULL</b>, the function opens the file specified by <i>lpFile</i>. If <i>lpOperation</i> is "open" or "explore", the function  attempts to open or explore the folder.

To obtain information about the application that is launched as a result of calling <b>ShellExecute</b>, use <a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>.

<div class="alert"><b>Note</b>  The <b>Launch folder windows in a separate process</b> setting in Folder Options affects <b>ShellExecute</b>. If that option is disabled (the default setting), <b>ShellExecute</b> uses an open Explorer window rather than launch a new one. If no Explorer window is open, <b>ShellExecute</b> launches a new one.</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ffb79c0f-aeda-4ea1-aea8-afb79109837f">CoInitializeEx</a>



<a href="https://msdn.microsoft.com/48af59ec-d646-454e-b699-389033812638">IShellExecuteHook</a>



<a href="https://msdn.microsoft.com/d774c3b2-4caf-460a-ac32-0ed603491d5f">Launching Applications (ShellExecute, ShellExecuteEx, SHELLEXECUTEINFO)</a>



<a href="https://msdn.microsoft.com/7850d19c-dadb-44a1-85d9-d5b897edb39f">ShellExecuteEx</a>
 

 

