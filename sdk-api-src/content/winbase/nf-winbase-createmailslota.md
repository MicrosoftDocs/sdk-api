---
UID: NF:winbase.CreateMailslotA
title: CreateMailslotA function
author: windows-sdk-content
description: Creates a mailslot with the specified name and returns a handle that a mailslot server can use to perform operations on the mailslot.
old-location: base\createmailslot.htm
old-project: ipc
ms.assetid: a2e8199f-4d00-4315-9562-ff30f4fafcb7
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: CreateMailslot, CreateMailslot function, CreateMailslotA, CreateMailslotW, MAILSLOT_WAIT_FOREVER, _win32_createmailslot, base.createmailslot, winbase/CreateMailslot, winbase/CreateMailslotA, winbase/CreateMailslotW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winbase.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: CreateMailslotW (Unicode) and CreateMailslotA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PRIORITY_HINT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
-	kernel32legacy.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
-	API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
-	API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
-	API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
-	CreateMailslot
-	CreateMailslotA
-	CreateMailslotW
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateMailslotA function


## -description


Creates a mailslot with the specified name and returns  a handle that a mailslot server can use to perform operations on the mailslot. The mailslot is local to the computer that creates it. An error occurs if a mailslot with the specified name already exists.


## -parameters




### -param lpName [in]

The name of the mailslot. This name must have the following form:

\\.\mailslot\[<i>path</i>]<i>name</i>

The name field must be unique. The name may include multiple levels of pseudo directories separated by backslashes. For example, both \\.\mailslot\example_mailslot_name and \\.\mailslot\abc\def\ghi are valid names.


### -param nMaxMessageSize [in]

The maximum size of a single message that can be written to the mailslot, in bytes. To specify that the message can be of any size, set this value to zero.


### -param lReadTimeout [in]

The time a read operation can wait for a message to be written to the mailslot before a time-out occurs, in milliseconds. The following values have special meanings.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
Returns immediately if no message is present. (The system does not treat an immediate return as an error.)

</td>
</tr>
<tr>
<td width="40%"><a id="MAILSLOT_WAIT_FOREVER"></a><a id="mailslot_wait_forever"></a><dl>
<dt><b>MAILSLOT_WAIT_FOREVER</b></dt>
<dt>((DWORD)-1)</dt>
</dl>
</td>
<td width="60%">
Waits forever for a message.

</td>
</tr>
</table>
 

This time-out value applies to all subsequent read operations and all inherited mailslot handles.


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure. The <b>bInheritHandle</b> member of the structure determines whether the returned handle can be inherited by child processes. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the handle cannot be inherited.


## -returns



If the function succeeds, the return value is a handle to the mailslot, for use in server mailslot operations.  The handle returned by this function is asynchronous, or overlapped.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



The mailslot exists until one of the following conditions is true:

<ul>
<li>The last (possibly inherited or duplicated) handle to it is closed using the 
<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.</li>
<li>The process owning the last (possibly inherited or duplicated) handle exits.</li>
</ul>
The system uses the second method to destroy mailslots.

To write a message to a mailslot, a process uses the 
<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> function, specifying the mailslot name by using one of the following formats.

<table>
<tr>
<th>Format</th>
<th>Usage</th>
</tr>
<tr>
<td>\\.\mailslot\<i>name</i></td>
<td>Retrieves a client handle to a local mailslot.</td>
</tr>
<tr>
<td>\\<i>computername</i>\mailslot\<i>name</i></td>
<td>Retrieves a client handle to a remote mailslot.</td>
</tr>
<tr>
<td>\\<i>domainname</i>\mailslot\<i>name</i></td>
<td>Retrieves a client handle to all mailslots with the specified name in the specified domain.</td>
</tr>
<tr>
<td>\\*\mailslot\<i>name</i></td>
<td>Retrieves a client handle to all mailslots with the specified name in the system's primary domain.</td>
</tr>
</table>
 

If <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> specifies a domain or uses the asterisk format to specify the system's primary domain, the application cannot write more than 424 bytes at a time to the mailslot. If the application attempts to do so, the <a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a> function fails and 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> returns <b>ERROR_BAD_NETPATH</b>.

An application must specify the <b>FILE_SHARE_READ</b> flag when using <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> to retrieve a client handle to a mailslot.

If <a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a> is called to access a non-existent mailslot, the  <b>ERROR_FILE_NOT_FOUND</b> error code will be set. 


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/7f5a3b36-9583-43fc-a977-321c00a48edb">Creating a Mailslot</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/80a96083-4de9-4422-9705-b8ad2b6cbd1b">CreateFile</a>



<a href="https://msdn.microsoft.com/873b4dbe-f808-4731-9314-a595ef7ef3c5">GetMailslotInfo</a>



<a href="https://msdn.microsoft.com/85f89fcc-2ab1-411b-ab3e-f1e9d425433f">Mailslot Functions</a>



<a href="https://msdn.microsoft.com/e23894ca-edc7-49e6-bcc4-c82f357ecedf">Mailslots Overview</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/4afcbbfb-fd04-4813-b139-4baffc2fdf3c">SetMailslotInfo</a>



<a href="https://msdn.microsoft.com/9d6fa723-fe3e-4052-b0b3-2686eee076a7">WriteFile</a>
 

 

