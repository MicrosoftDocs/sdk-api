---
UID: NF:winbase.CreateMailslotA
title: CreateMailslotA function (winbase.h)
description: Creates a mailslot with the specified name and returns a handle that a mailslot server can use to perform operations on the mailslot. (ANSI)
helpviewer_keywords: ["CreateMailslotA", "MAILSLOT_WAIT_FOREVER", "winbase/CreateMailslotA"]
old-location: base\createmailslot.htm
tech.root: base
ms.assetid: a2e8199f-4d00-4315-9562-ff30f4fafcb7
ms.date: 12/05/2018
ms.keywords: CreateMailslot, CreateMailslot function, CreateMailslotA, CreateMailslotW, MAILSLOT_WAIT_FOREVER, _win32_createmailslot, base.createmailslot, winbase/CreateMailslot, winbase/CreateMailslotA, winbase/CreateMailslotW
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CreateMailslotA
 - winbase/CreateMailslotA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - api-ms-win-core-kernel32-legacy-l1-1-6.dll
 - Kernel32.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-0.dll
 - kernel32legacy.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-1.dll
 - API-MS-Win-Core-Kernel32-Legacy-l1-1-2.dll
 - API-MS-Win-DownLevel-Kernel32-l2-1-0.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-3.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-4.dll
 - API-MS-Win-Core-Kernel32-Legacy-L1-1-5.dll
api_name:
 - CreateMailslot
 - CreateMailslotA
 - CreateMailslotW
---

# CreateMailslotA function


## -description

Creates a mailslot with the specified name and returns  a handle that a mailslot server can use to perform operations on the mailslot. The mailslot is local to the computer that creates it. An error occurs if a mailslot with the specified name already exists.

## -parameters

### -param lpName [in]

The name of the mailslot. This name must have the following form:

\\\\.\mailslot\\[<i>path</i>]<i>name</i>

The name field must be unique. The name may include multiple levels of pseudo directories separated by backslashes. For example, both \\\\.\mailslot\example_mailslot_name and \\\\.\mailslot\abc\def\ghi are valid names.

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
<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a> structure. The <b>bInheritHandle</b> member of the structure determines whether the returned handle can be inherited by child processes. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the handle cannot be inherited.

## -returns

If the function succeeds, the return value is a handle to the mailslot, for use in server mailslot operations.  The handle returned by this function is asynchronous, or overlapped.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -remarks

The mailslot exists until one of the following conditions is true:

<ul>
<li>The last (possibly inherited or duplicated) handle to it is closed using the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function.</li>
<li>The process owning the last (possibly inherited or duplicated) handle exits.</li>
</ul>
The system uses the second method to destroy mailslots.

To write a message to a mailslot, a process uses the 
<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> function, specifying the mailslot name by using one of the following formats.

<table>
<tr>
<th>Format</th>
<th>Usage</th>
</tr>
<tr>
<td>\\.\mailslot&#92;<i>name</i></td>
<td>Retrieves a client handle to a local mailslot.</td>
</tr>
<tr>
<td>&#92;&#92;<i>computername</i>\mailslot&#92;<i>name</i></td>
<td>Retrieves a client handle to a remote mailslot.</td>
</tr>
<tr>
<td>&#92;&#92;<i>domainname</i>\mailslot&#92;<i>name</i></td>
<td>Retrieves a client handle to all mailslots with the specified name in the specified domain.</td>
</tr>
<tr>
<td>\\*\mailslot&#92;<i>name</i></td>
<td>Retrieves a client handle to all mailslots with the specified name in the system's primary domain.</td>
</tr>
</table>
 

If <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> specifies a domain or uses the asterisk format to specify the system's primary domain, the application cannot write more than 424 bytes at a time to the mailslot. If the application attempts to do so, the <a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a> function fails and 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a> returns <b>ERROR_BAD_NETPATH</b>.

An application must specify the <b>FILE_SHARE_READ</b> flag when using <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> to retrieve a client handle to a mailslot.

If <a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a> is called to access a non-existent mailslot, the  <b>ERROR_FILE_NOT_FOUND</b> error code will be set. 


#### Examples

For an example, see 
<a href="/windows/desktop/ipc/creating-a-mailslot">Creating a Mailslot</a>.

<div class="code"></div>




> [!NOTE]
> The winbase.h header defines CreateMailslot as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-createfilea">CreateFile</a>



<a href="/windows/desktop/api/winbase/nf-winbase-getmailslotinfo">GetMailslotInfo</a>



<a href="/windows/desktop/ipc/mailslot-functions">Mailslot Functions</a>



<a href="/windows/desktop/ipc/mailslots">Mailslots Overview</a>



<a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>



<a href="/windows/desktop/api/winbase/nf-winbase-setmailslotinfo">SetMailslotInfo</a>



<a href="/windows/desktop/api/fileapi/nf-fileapi-writefile">WriteFile</a>
