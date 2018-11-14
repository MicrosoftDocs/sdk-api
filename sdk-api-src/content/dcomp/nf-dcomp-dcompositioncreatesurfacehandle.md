---
UID: NF:dcomp.DCompositionCreateSurfaceHandle
title: DCompositionCreateSurfaceHandle function
author: windows-sdk-content
description: Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.
old-location: directcomp\dcompositioncreatesurfacehandle.htm
tech.root: directcomp
ms.assetid: 550BA10B-D582-4A57-A69D-3EFFC7313D8F
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: COMPOSITIONSURFACE_ALL_ACCESS, COMPOSITIONSURFACE_READ, COMPOSITIONSURFACE_WRITE, DCompositionCreateSurfaceHandle, DCompositionCreateSurfaceHandle function [DirectComposition], dcomp/DCompositionCreateSurfaceHandle, directcomp.dcompositioncreatesurfacehandle
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dcomp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Dcomp.lib
req.dll: Dcomp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dcomp.dll
 - Ext-MS-OneCore-DComp-L1-1-0.dll
api_name:
 - DCompositionCreateSurfaceHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DCompositionCreateSurfaceHandle
: 
---

# DCompositionCreateSurfaceHandle function


## -description


Creates a new composition surface object that can be bound to a
Microsoft DirectX swap chain or swap buffer and associated
with a visual.


## -parameters




### -param desiredAccess [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The requested access to the composition surface object. It can be one of the following values:

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id=""></a><dl>
<dt><b></b></dt>
<dt>0x0000L</dt>
</dl>
</td>
<td width="60%">
No access.

</td>
</tr>
<tr>
<td width="40%"><a id="COMPOSITIONSURFACE_READ"></a><a id="compositionsurface_read"></a><dl>
<dt><b>COMPOSITIONSURFACE_READ</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
Read access. For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="COMPOSITIONSURFACE_WRITE"></a><a id="compositionsurface_write"></a><dl>
<dt><b>COMPOSITIONSURFACE_WRITE</b></dt>
<dt>0x0002L</dt>
</dl>
</td>
<td width="60%">
Write access. For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="COMPOSITIONSURFACE_ALL_ACCESS"></a><a id="compositionsurface_all_access"></a><dl>
<dt><b>COMPOSITIONSURFACE_ALL_ACCESS</b></dt>
<dt>0x0003L</dt>
</dl>
</td>
<td width="60%">
Read/write access. Always specify this flag except when duplicating a surface in another process, in which case set <i>desiredAccess</i> to 0.

</td>
</tr>
</table>
 


### -param securityAttributes [in, optional]

Type: <b><a href="https://msdn.microsoft.com/56b5b350-f4b7-47af-b5f8-6a35f32c1009">SECURITY_ATTRIBUTES</a>*</b>

Contains the security descriptor for the composition surface object, and specifies whether the handle of the composition surface object is inheritable when a child process is created. If this parameter is NULL, the composition surface object is created with default security attributes  that grant read and write access to the current process,  but do not enable child processes to  inherit the handle.


### -param surfaceHandle [out]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HANDLE</a>*</b>

The handle of the new composition surface object. This parameter must not be NULL.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="https://msdn.microsoft.com/8DFBFC34-DBD0-4731-8305-B33E90C96C54">DirectComposition Error Codes</a>  for a list of error codes.  



