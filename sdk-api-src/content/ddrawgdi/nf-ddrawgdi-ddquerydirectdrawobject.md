---
UID: NF:ddrawgdi.DdQueryDirectDrawObject
title: DdQueryDirectDrawObject function (ddrawgdi.h)
description: Wrapper for the NtGdiDdQueryDirectDrawObject function and queries a previously created kernel-mode representation for capabilities. GdiEntry2 is defined as an alias for this function.
helpviewer_keywords: ["DdQueryDirectDrawObject","DdQueryDirectDrawObject function [Windows API]","GdiEntry2","_dxgkernel_ddquerydirectdrawobject","ddrawgdi/DdQueryDirectDrawObject","ddrawgdi/GdiEntry2","winprog._dxgkernel_ddquerydirectdrawobject","winui._dxgkernel_ddquerydirectdrawobject"]
old-location: winprog\_dxgkernel_ddquerydirectdrawobject.htm
tech.root: winprog
ms.assetid: VS|winui|~\winui\windowsuserinterface\lowlevelclientsupport\graphics\ddquerydirectdrawobject.htm
ms.date: 12/05/2018
ms.keywords: DdQueryDirectDrawObject, DdQueryDirectDrawObject function [Windows API], GdiEntry2, _dxgkernel_ddquerydirectdrawobject, ddrawgdi/DdQueryDirectDrawObject, ddrawgdi/GdiEntry2, winprog._dxgkernel_ddquerydirectdrawobject, winui._dxgkernel_ddquerydirectdrawobject
req.header: ddrawgdi.h
req.include-header: 
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DdQueryDirectDrawObject
 - ddrawgdi/DdQueryDirectDrawObject
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ddrawgdi.h
 - Ext-MS-Win-GDI-Internal-Desktop-L1-1-0.dll
 - GDI32.dll
 - GDI32Full.dll
api_name:
 - DdQueryDirectDrawObject
 - GdiEntry2
---

# DdQueryDirectDrawObject function


## -description

<p class="CCE_Message">[This function is subject to change with each operating system revision. Instead, use the Microsoft DirectDraw and Microsoft Direct3DAPIs; these APIs insulate applications from such operating system changes, and hide many other difficulties involved in interacting directly with display drivers.]

Wrapper for the <a href="/windows/desktop/DevNotes/-dxgkernel-ntgdiddquerydirectdrawobject">NtGdiDdQueryDirectDrawObject</a> function and queries a previously created kernel-mode representation for capabilities.


<b>GdiEntry2</b> is defined as an alias for this function.

## -parameters

### -param pDirectDrawGlobal

Pointer to a user-mode DirectDraw object for which a kernel-side object was previously created with <a href="/windows/desktop/api/ddrawgdi/nf-ddrawgdi-ddcreatedirectdrawobject">DdCreateDirectDrawObject</a>.

### -param pHalInfo

Pointer to a <b>DDHALINFO</b> structure that will be filled with the device's capabilities. See DDK documentation for details.

### -param pDDCallbacks

Pointer to a table of callback pointers. The table is filled with pointers to functions within Gdi32.dll that imitate a DirectDraw display driver. This callback table is identical to the DDHAL_DDCALLBACKS structure, which maps to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_callbacks">DD_CALLBACKS</a> structure discussed in the DDK documentation.

### -param pDDSurfaceCallbacks

Pointer to a table of surface callback pointers. The table is filled with pointers to functions within Gdi32.dll that imitate a DirectDraw display driver. This callback table is identical to the DDHAL_DDSURFACECALLBACKS structure, which maps to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_surfacecallbacks">DD_SURFACECALLBACKS</a> structure discussed in the DDK documentation.

### -param pDDPaletteCallbacks

Pointer to a table of palette callback pointers. The table is filled with pointers to functions within Gdi32.dll that imitate a DirectDraw display driver. This callback table is identical to the DDHAL_DDPALETTECALLBACKS structure, which maps to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_palettecallbacks">DD_PALETTECALLBACKS</a> structure discussed in the DDK documentation.

### -param pD3dCallbacks

Pointer to a table of Direct3D callback pointers. The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver. This callback table is identical to the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_callbacks">D3DHAL_CALLBACKS</a> structure discussed in the DDK documentation.

### -param pD3dDriverData

Pointer to <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata">D3DHAL_GLOBALDRIVERDATA</a> data, as described in the DDK documentation.

### -param pD3dBufferCallbacks

Pointer to a table of callback pointers. The table is filled with pointers to functions within Gdi32.dll that imitate a Direct3D display driver. This callback table is identical to the DDHAL_DDEXEBUFCALLBACKS structure, which maps to the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_d3dbufcallbacks">DD_D3DBUFCALLBACKS</a> structure discussed in the DDK documentation, except that members XxxD3DBuffer in <b>DD_D3DBUFCALLBACKS</b> are replaced with XxxExecuteBuffer in DDHAL_DDEXEBUFCALLBACKS.

### -param pD3dTextureFormats

Pointer to an array of <b>DDSURFACEDESC</b> structures that define the set of permissible texture formats.

### -param pdwFourCC

Pointer to a list of supported <a href="/windows/desktop/DirectShow/fourcc-codes">Four-Character Codes (FOURCC)</a> surface formats. Can be <b>NULL</b>.

### -param pvmList

Pointer to a list of video memory heap descriptors. Can be <b>NULL</b>. This parameter is not used because video memory management is handled entirely within kernel mode.

## -returns

If successful, this function returns <b>TRUE</b>; otherwise it returns <b>FALSE</b>.

## -remarks

A call to this function is designed to be made in a two-step process. In the first step, <i>pdwFourCC</i>, <i>pvmList</i> and <i>pD3dTextureFormats</i> should be <b>NULL</b>, and <b>DdQueryDirectDrawObject</b> will fill in <b>DDHALINFO</b>.<b>ddCaps</b>.<b>dwNumFourCCCodes</b>, <b>DDHALINFO</b>.<b>vmiData</b>.<b>dwNumHeaps</b>, and <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_globaldriverdata">D3DHAL_GLOBALDRIVERDATA</a>.<b>dwNumTextureFormats</b> with the number of entries that are to be returned. In the second call, the caller should allocate arrays of the indicated size and pass those pointers instead of <b>NULL</b> values in the <i>pdwFourCC</i>, <i>pvmList</i> and <i>pD3dTextureFormats</i> parameters. The arrays will then be populated with appropriate data.
        

Applications are advised to use the 
DirectDraw and 
<a href="/windows/desktop/direct3d10/d3d10-graphics-reference">Direct3D</a> APIs to create and manage graphics device objects. These constructs abstract the device creation process in a simplified and operating-system-independent way.

## -see-also

<a href="/windows/desktop/DevNotes/-dxgkernel-low-level-client-support">Graphics Low Level Client Support</a>