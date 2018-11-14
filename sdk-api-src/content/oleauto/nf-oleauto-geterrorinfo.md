---
UID: NF:oleauto.GetErrorInfo
title: GetErrorInfo function
author: windows-sdk-content
description: Obtains the error information pointer set by the previous call to SetErrorInfo in the current logical thread.
old-location: automat\geterrorinfo.htm
tech.root: automat
ms.assetid: 03317526-8c4f-4173-bc10-110c8112676a
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: GetErrorInfo, GetErrorInfo function [Automation], _oa96_GetErrorInfo, automat.geterrorinfo, oleauto/GetErrorInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: oleauto.h
req.include-header: 
req.target-type: Windows
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
req.lib: OleAut32.lib
req.dll: OleAut32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - OleAut32.dll
 - API-MS-Win-Downlevel-OLE32-l1-1-1.dll
 - ComBase.dll
api_name:
 - GetErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- GetErrorInfo
: 
---

# GetErrorInfo function


## -description


Obtains the error information pointer set by the previous call to <a href="https://msdn.microsoft.com/8eaacfac-fc37-4eaa-870b-10b99d598d66">SetErrorInfo</a> in the current logical thread.


## -parameters




### -param dwReserved [in]

Reserved for future use. Must be zero.




### -param pperrinfo [out]

An error object.


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
There was no error object to return.


</td>
</tr>
</table>
 




## -remarks



This function returns a pointer to the most recently set <a href="https://msdn.microsoft.com/4dda6909-2d9a-4727-ae0c-b5f90dcfa447">IErrorInfo</a> pointer in the current logical thread. It transfers ownership of the error object to the caller, and clears the error state for the thread.

Making a COM call that goes through a proxy-stub will clear any existing error object for the calling thread. A called object should not make any such calls after calling <a href="https://msdn.microsoft.com/8eaacfac-fc37-4eaa-870b-10b99d598d66">SetErrorInfo</a> and before returning. The caller should not make any such calls after the call returns and before calling <b>GetErrorInfo</b>. As a rule of thumb, an interface method should return as soon as possible after calling <b>SetErrorInfo</b>, and the caller should call <b>GetErrorInfo</b> as soon as possible after the call returns.




