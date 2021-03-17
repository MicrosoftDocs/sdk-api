---
UID: NF:handleapi.GetHandleInformation
title: GetHandleInformation function (handleapi.h)
description: Retrieves certain properties of an object handle.
helpviewer_keywords: ["GetHandleInformation","GetHandleInformation function","HANDLE_FLAG_INHERIT","HANDLE_FLAG_PROTECT_FROM_CLOSE","_win32_gethandleinformation","base.gethandleinformation","handleapi/GetHandleInformation"]
old-location: base\gethandleinformation.htm
tech.root: winprog
ms.assetid: a0f50a0d-739d-411b-8144-77b775476d26
ms.date: 12/05/2018
ms.keywords: GetHandleInformation, GetHandleInformation function, HANDLE_FLAG_INHERIT, HANDLE_FLAG_PROTECT_FROM_CLOSE, _win32_gethandleinformation, base.gethandleinformation, handleapi/GetHandleInformation
req.header: handleapi.h
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
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - GetHandleInformation
 - handleapi/GetHandleInformation
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Kernel32.dll
 - API-MS-Win-Core-handle-l1-1-0.dll
 - KernelBase.dll
 - API-MS-Win-DownLevel-Kernel32-l1-1-0.dll
 - MinKernelBase.dll
api_name:
 - GetHandleInformation
---

# GetHandleInformation function


## -description

Retrieves certain properties of an object handle.

## -parameters

### -param hObject [in]

A handle to an object whose information is to be retrieved. 




You can specify a handle to one of the following types of objects: access token, console input buffer, console screen buffer, event, file, file mapping, job, mailslot, mutex, pipe, printer, process, registry key, semaphore, serial communication device, socket, thread, or waitable timer.

### -param lpdwFlags [out]

A pointer to a variable that receives a set of bit flags that specify properties of the object handle or 0. The following values are defined. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="HANDLE_FLAG_INHERIT"></a><a id="handle_flag_inherit"></a><dl>
<dt><b>HANDLE_FLAG_INHERIT</b></dt>
<dt>0x00000001</dt>
</dl>
</td>
<td width="60%">
If this flag is set, a child process created with the <i>bInheritHandles</i> parameter of 
<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a> set to <b>TRUE</b> will inherit the object handle.

</td>
</tr>
<tr>
<td width="40%"><a id="HANDLE_FLAG_PROTECT_FROM_CLOSE"></a><a id="handle_flag_protect_from_close"></a><dl>
<dt><b>HANDLE_FLAG_PROTECT_FROM_CLOSE</b></dt>
<dt>0x00000002</dt>
</dl>
</td>
<td width="60%">
If this flag is set, calling the 
<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a> function will not close the object handle.

</td>
</tr>
</table>

## -returns

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
<a href="/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.

## -see-also

<a href="/windows/desktop/api/handleapi/nf-handleapi-closehandle">CloseHandle</a>



<a href="/windows/desktop/api/processthreadsapi/nf-processthreadsapi-createprocessa">CreateProcess</a>



<a href="/windows/desktop/SysInfo/handle-and-object-functions">Handle and
		  Object Functions</a>



<a href="/windows/desktop/api/handleapi/nf-handleapi-sethandleinformation">SetHandleInformation</a>