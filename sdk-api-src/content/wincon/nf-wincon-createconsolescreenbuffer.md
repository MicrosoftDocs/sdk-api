---
UID: NF:wincon.CreateConsoleScreenBuffer
title: CreateConsoleScreenBuffer function
author: windows-driver-content
description: Creates a console screen buffer.
old-location: consoles\createconsolescreenbuffer.htm
old-project: consoles
ms.assetid: 98bb74e4-dad2-4615-9263-48ba778a06ff
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: CreateConsoleScreenBuffer, CreateConsoleScreenBuffer function [Consoles], FILE_SHARE_READ, FILE_SHARE_WRITE, _win32_createconsolescreenbuffer, base.createconsolescreenbuffer, consoles.createconsolescreenbuffer, wincon/CreateConsoleScreenBuffer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: wincon.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
req.typenames: WICMetadataPattern
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Kernel32.dll
-	API-MS-Win-Core-Console-l2-1-0.dll
-	KernelBase.dll
-	API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
api_name:
-	CreateConsoleScreenBuffer
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# CreateConsoleScreenBuffer function


## -description


Creates a console screen buffer.


## -parameters




### -param dwDesiredAccess [in]

The access to the console screen buffer. For a list of access rights, see 
<a href="https://msdn.microsoft.com/f9a50063-8fc8-4cd1-8f24-9ae3946d3119">Console Buffer Security and Access Rights</a>.


### -param dwShareMode [in]

This parameter can be zero, indicating that the buffer cannot be shared, or it can be one or more of the following values. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_READ"></a><a id="file_share_read"></a><dl>
<dt><b>FILE_SHARE_READ</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
Other open operations can be performed on the console screen buffer for read access.

</td>
</tr>
<tr>
<td width="40%"><a id="FILE_SHARE_WRITE"></a><a id="file_share_write"></a><dl>
<dt><b>FILE_SHARE_WRITE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
Other open operations can be performed on the console screen buffer for write access.

</td>
</tr>
</table>
 


### -param lpSecurityAttributes [in, optional]

A pointer to a 
<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a> structure that determines whether the returned handle can be inherited by child processes. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the handle cannot be inherited. 


The <b>lpSecurityDescriptor</b> member of the structure specifies a security descriptor for the new console screen buffer. If <i>lpSecurityAttributes</i> is <b>NULL</b>, the console screen buffer gets a default security descriptor. The ACLs in the default security descriptor for a console screen buffer come from the primary or impersonation token of the creator.
					


### -param dwFlags [in]

The type of console screen buffer to create. The only supported screen buffer type is <b>CONSOLE_TEXTMODE_BUFFER</b>.


### -param lpScreenBufferData

Reserved; should be <b>NULL</b>.


## -returns



If the function succeeds, the return value is a handle to the new console screen buffer.

If the function fails, the return value is <b>INVALID_HANDLE_VALUE</b>. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -remarks



A console can have multiple screen buffers but only one active screen buffer. Inactive screen buffers can be accessed for reading and writing, but only the active screen buffer is displayed. To make the new screen buffer the active screen buffer, use the 
<a href="https://msdn.microsoft.com/c026cb94-c8ec-44ee-b432-3870ae3006c2">SetConsoleActiveScreenBuffer</a> function.

The calling process can use the returned handle in any function that requires a handle to a console screen buffer, subject to the limitations of access specified by the <i>dwDesiredAccess</i> parameter.

The calling process can use the <a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a> function to create a duplicate screen buffer handle that has different access or inheritability from the original handle. However, <b>DuplicateHandle</b> cannot be used to create a duplicate that is valid for a different process (except through inheritance).

To close the console screen buffer handle, use the <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a> function.


#### Examples

For an example, see 
<a href="https://msdn.microsoft.com/eaa57723-f003-4e90-8156-be8c3b42b912">Reading and Writing Blocks of Characters and Attributes</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>



<a href="https://msdn.microsoft.com/2a0e5dcc-be48-42ab-a05a-96f68d012a67">Console Functions</a>



<a href="https://msdn.microsoft.com/f94995fc-5f5f-4fcd-969d-7e10020634c2">Console Screen Buffers</a>



<a href="https://msdn.microsoft.com/9c8da574-5bda-49f1-a6b6-c026639d6504">DuplicateHandle</a>



<a href="https://msdn.microsoft.com/eafe819e-a99a-4ce1-8898-8860444a31af">GetConsoleScreenBufferInfo</a>



<a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/c026cb94-c8ec-44ee-b432-3870ae3006c2">SetConsoleActiveScreenBuffer</a>



<a href="https://msdn.microsoft.com/50bf1973-5604-42fe-bbeb-611ddc240bdd">SetConsoleScreenBufferSize</a>
 

 

