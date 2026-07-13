---
UID: NF:dcomp.DCompositionCreateSurfaceHandle
title: DCompositionCreateSurfaceHandle function (dcomp.h)
description: Creates a new composition surface object that can be bound to a Microsoft DirectX swap chain or swap buffer and associated with a visual.
helpviewer_keywords: ["COMPOSITIONSURFACE_ALL_ACCESS","COMPOSITIONOBJECT_ALL_ACCESS","COMPOSITIONSURFACE_READ","COMPOSITIONOBJECT_READ","COMPOSITIONSURFACE_WRITE","COMPOSITIONOBJECT_WRITE","DCompositionCreateSurfaceHandle","DCompositionCreateSurfaceHandle function [DirectComposition]","dcomp/DCompositionCreateSurfaceHandle","directcomp.dcompositioncreatesurfacehandle"]
old-location: directcomp\dcompositioncreatesurfacehandle.htm
tech.root: directcomp
ms.assetid: 550BA10B-D582-4A57-A69D-3EFFC7313D8F
ms.date: 12/05/2018
ms.keywords: COMPOSITIONSURFACE_ALL_ACCESS, COMPOSITIONOBJECT_ALL_ACCESS, COMPOSITIONSURFACE_READ, COMPOSITIONOBJECT_READ, COMPOSITIONSURFACE_WRITE, COMPOSITIONOBJECT_WRITE, DCompositionCreateSurfaceHandle, DCompositionCreateSurfaceHandle function [DirectComposition], dcomp/DCompositionCreateSurfaceHandle, directcomp.dcompositioncreatesurfacehandle
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DCompositionCreateSurfaceHandle
 - dcomp/DCompositionCreateSurfaceHandle
dev_langs:
 - c++
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
---

# DCompositionCreateSurfaceHandle function


## -description

Creates a new composition surface object that can be bound to a
Microsoft DirectX swap chain or swap buffer and associated
with a visual.

## -parameters

### -param desiredAccess [in]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">DWORD</a></b>

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
<td width="40%"><a id="COMPOSITIONOBJECT_READ"></a><a id="compositionobject_read"></a><dl>
<dt><b>COMPOSITIONOBJECT_READ</b></dt>
<dt>0x0001L</dt>
</dl>
</td>
<td width="60%">
Read access. For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="COMPOSITIONOBJECT_WRITE"></a><a id="compositionobject_write"></a><dl>
<dt><b>COMPOSITIONOBJECT_WRITE</b></dt>
<dt>0x0002L</dt>
</dl>
</td>
<td width="60%">
Write access. For internal use only.

</td>
</tr>
<tr>
<td width="40%"><a id="COMPOSITIONOBJECT_ALL_ACCESS"></a><a id="compositionobject_all_access"></a><dl>
<dt><b>COMPOSITIONOBJECT_ALL_ACCESS</b></dt>
<dt>0x0003L</dt>
</dl>
</td>
<td width="60%">
Read/write access. Always specify this flag except when duplicating a surface in another process, in which case set <i>desiredAccess</i> to 0.

</td>
</tr>
</table>

### -param securityAttributes [in, optional]

Type: <b><a href="/windows/win32/api/wtypesbase/ns-wtypesbase-security_attributes">SECURITY_ATTRIBUTES</a>*</b>

Contains the security descriptor for the composition surface object, and specifies whether the handle of the composition surface object is inheritable when a child process is created. If this parameter is NULL, the composition surface object is created with default security attributes  that grant read and write access to the current process,  but do not enable child processes to  inherit the handle.

### -param surfaceHandle [out]

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HANDLE</a>*</b>

The handle of the new composition surface object. This parameter must not be NULL.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If the function succeeds, it returns S_OK. Otherwise, it returns an <b>HRESULT</b> error code. See <a href="/windows/desktop/directcomp/directcomposition-error-codes">DirectComposition Error Codes</a>  for a list of error codes.
