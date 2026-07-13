---
UID: NF:fltuser.FilterLoad
title: FilterLoad function (fltuser.h)
description: The FilterLoad function dynamically loads a minifilter driver into the system.
helpviewer_keywords: ["FilterLoad","FilterLoad function [Installable File System Drivers]","FltWin32ApiRef_273c18c5-9474-4605-80a1-1bc4cb9e4e7b.xml","fltuser/FilterLoad","ifsk.filterload"]
old-location: ifsk\filterload.htm
tech.root: ifsk
ms.assetid: 248e05e6-570a-45fc-8b63-16625ffda1dd
ms.date: 12/05/2018
ms.keywords: FilterLoad, FilterLoad function [Installable File System Drivers], FltWin32ApiRef_273c18c5-9474-4605-80a1-1bc4cb9e4e7b.xml, fltuser/FilterLoad, ifsk.filterload
req.header: fltuser.h
req.include-header: Fltuser.h
req.target-type: Universal
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
req.lib: FltLib.lib
req.dll: FltLib.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - FilterLoad
 - fltuser/FilterLoad
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - FltLib.dll
api_name:
 - FilterLoad
---

# FilterLoad function


## -description

The <b>FilterLoad</b> function dynamically loads a minifilter driver into the system.

## -parameters

### -param lpFilterName [in]

Pointer to a null-terminated wide-character string that specifies the service name of the minifilter driver. This parameter is required and cannot be <b>NULL</b> or an empty string.

## -returns

<b>FilterLoad</b> returns S_OK if successful. Otherwise, it returns one of the following error values: 

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_ALREADY_EXISTS)</b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver is already running. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_FILE_NOT_FOUND)</b></dt>
</dl>
</td>
<td width="60%">
No matching minifilter driver was found. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_SERVICE_ALREADY_RUNNING)</b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver is already running. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_BAD_EXE_FORMAT)</b></dt>
</dl>
</td>
<td width="60%">
The load image for the minifilter driver specified by <i>lpFilterName</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_BAD_DRIVER)</b></dt>
</dl>
</td>
<td width="60%">
The load image for the minifilter driver specified by <i>lpFilterName</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>HRESULT_FROM_WIN32 (ERROR_INVALID_IMAGE_HASH)</b></dt>
</dl>
</td>
<td width="60%">
The minifilter driver has an invalid digital signature.

</td>
</tr>
</table>

## -remarks

<b>FilterLoad</b> is the Win32 equivalent of <a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltloadfilter">FltLoadFilter</a>. 

A user-mode application that has a dependency on a kernel-mode minifilter driver can load the minifilter driver by calling <b>FilterLoad</b>. 

Callers of <b>FilterLoad</b> must have <b>SeLoadDriverPrivilege</b> (the LUID of SE_LOAD_DRIVER_PRIVILEGE) to load or unload a minifilter driver. This privilege is named by the SE_LOAD_DRIVER_NAME name constant. (Privileges are described in the Microsoft Windows Software Development Kit (SDK) for Windows 7 and .NET Framework 4.0 documentation.) 

To unload the minifilter driver, call <a href="/windows/desktop/api/fltuser/nf-fltuser-filterunload">FilterUnload</a>.

## -see-also

<a href="/windows/desktop/api/fltuser/nf-fltuser-filterunload">FilterUnload</a>



<a href="/windows-hardware/drivers/ddi/content/fltkernel/nf-fltkernel-fltloadfilter">FltLoadFilter</a>



<a href="/windows/win32/api/winerror/nf-winerror-hresult_from_win32">HRESULT_FROM_WIN32</a>