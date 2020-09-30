---
UID: NS:ddrawint._DD_GETDRIVERINFODATA
title: DD_GETDRIVERINFODATA (ddrawint.h)
description: The DD_GETDRIVERINFODATA structure is used to pass data to and from the DdGetDriverInfo callback routine.
helpviewer_keywords: ["*PDD_GETDRIVERINFODATA","DD_GETDRIVERINFODATA","DD_GETDRIVERINFODATA structure [Display Devices]","PDD_GETDRIVERINFODATA","PDD_GETDRIVERINFODATA structure pointer [Display Devices]","ddrawint/DD_GETDRIVERINFODATA","ddrawint/PDD_GETDRIVERINFODATA","ddstrcts_1c0cf063-699e-497d-8554-db34185a1668.xml","display.dd_getdriverinfodata"]
old-location: display\dd_getdriverinfodata.htm
tech.root: display
ms.assetid: 15a4e80d-2186-4683-a05f-405ca75044e5
ms.date: 12/05/2018
ms.keywords: '*PDD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA structure [Display Devices], PDD_GETDRIVERINFODATA, PDD_GETDRIVERINFODATA structure pointer [Display Devices], ddrawint/DD_GETDRIVERINFODATA, ddrawint/PDD_GETDRIVERINFODATA, ddstrcts_1c0cf063-699e-497d-8554-db34185a1668.xml, display.dd_getdriverinfodata'
req.header: ddrawint.h
req.include-header: Winddi.h
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: '*PDD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA'
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _DD_GETDRIVERINFODATA
 - ddrawint/_DD_GETDRIVERINFODATA
 - PDD_GETDRIVERINFODATA
 - ddrawint/PDD_GETDRIVERINFODATA
 - DD_GETDRIVERINFODATA
 - ddrawint/DD_GETDRIVERINFODATA
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETDRIVERINFODATA
---

# DD_GETDRIVERINFODATA structure


## -description

The DD_GETDRIVERINFODATA structure is used to pass data to and from the <i>DdGetDriverInfo</i> callback routine.

## -struct-fields

### -field dhpdev

Handle to the driver's <a href="/windows-hardware/drivers/display/pdev-negotiation">PDEV</a>. Microsoft Windows 2000 and later only.

### -field dwSize

Specifies the size in bytes of this DD_GETDRIVERINFODATA structure.

### -field dwFlags

Currently unused and is set to zero.

### -field guidInfo

Specifies the GUID of the Microsoft DirectX support for which the driver is being queried. In a Windows 2000 and later Microsoft DirectDraw driver, this member can be one of the following values (in alphabetic order): 

<table>
<tr>
<th>GUID</th>
<th>Description</th>
</tr>
<tr>
<td>
GUID_ColorControlCallbacks

</td>
<td>
Queries whether the driver supports <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_colorcb_colorcontrol">DdControlColor</a>. If the driver does support it, the driver should initialize and return a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_colorcontrolcallbacks">DD_COLORCONTROLCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_callbacks">D3DHAL_CALLBACKS</a> structure. If the driver does not provide any of this support, it should initialize and return a D3DHAL_CALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DCallbacks2

</td>
<td>
Obsolete.

</td>
</tr>
<tr>
<td>
GUID_D3DCallbacks3

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_callbacks3">D3DHAL_CALLBACKS3</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_CALLBACKS3 structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DCaps

</td>
<td>
Obsolete.

</td>
</tr>
<tr>
<td>
GUID_D3DExtendedCaps

</td>
<td>
Queries whether the driver supports any of the Microsoft Direct3D functionality specified through the <a href="/windows-hardware/drivers/ddi/content/d3dhal/ns-d3dhal-_d3dhal_d3dextendedcaps">D3DHAL_D3DEXTENDEDCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_D3DEXTENDEDCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DParseUnknownCommandCallback

</td>
<td>
Provides the Direct3D portion of the driver with the Direct3D runtime's <i>D3dParseUnknownCommandCallback</i>. The driver's <a href="/windows-hardware/drivers/ddi/content/d3dhal/nc-d3dhal-lpd3dhal_drawprimitives2cb">D3dDrawPrimitives2</a> callback calls <i>D3dParseUnknownCommandCallback</i> to parse commands from the command buffer that the driver doesn't understand.DirectDraw passes a pointer to this function in the buffer to which <b>lpvData</b> points. If the driver supports this aspect of Direct3D, it should store the pointer.

</td>
</tr>
<tr>
<td>
GUID_GetHeapAlignment

</td>
<td>
Queries whether the driver supports surface alignment requirements on a per-heap basis. If the driver does provide this support, it should initialize and return a <a href="/windows/desktop/api/dmemmgr/ns-dmemmgr-dd_getheapalignmentdata">DD_GETHEAPALIGNMENTDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_kernelcallbacks">DD_KERNELCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_KERNELCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCaps

</td>
<td>
Queries whether the driver supports any of the kernel-mode capabilities specified through the <a href="/windows/desktop/api/ddkernel/ns-ddkernel-ddkernelcaps">DDKERNELCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDKERNELCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MiscellaneousCallbacks

</td>
<td>
Queries whether the driver supports <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getavaildrivermemory">DdGetAvailDriverMemory</a>. If the driver does support it, the driver should initialize and return a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneouscallbacks">DD_MISCELLANEOUSCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_Miscellaneous2Callbacks

</td>
<td>
Queries whether the driver supports the additional miscellaneous functionality specified in the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_miscellaneous2callbacks">DD_MISCELLANEOUS2CALLBACKS</a> structure. If the driver does support any of this support, the driver should initialize and return a DD_MISCELLANEOUS2CALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MotionCompCallbacks

</td>
<td>
Queries whether the driver supports the motion compensation functionality specified through the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_motioncompcallbacks">DD_MOTIONCOMPCALLBACKS</a> structure. If the driver does provide any of this support, is should initialize and return a DD_MOTIONCOMPCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NonLocalVidMemCaps

</td>
<td>
Queries whether the driver supports any of the nonlocal display memory capabilities specified through the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_nonlocalvidmemcaps">DD_NONLOCALVIDMEMCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NONLOCALVIDMEMCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntcallbacks">DD_NTCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTPrivateDriverCaps

</td>
<td>
Queries whether the driver supports the Windows 98/Me-style surface creation techniques specified through the <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_ntprivatedrivercaps">DD_NTPRIVATEDRIVERCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTPRIVATEDRIVERCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_UpdateNonLocalHeap

</td>
<td>
Queries whether the driver supports retrieval of the base addresses of each nonlocal heap in turn. If the driver does provide this support, it should initialize and return a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_updatenonlocalheapdata">DD_UPDATENONLOCALHEAPDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCallbacks

</td>
<td>
Queries whether the driver supports the <a href="/windows-hardware/drivers/">video port extensions (VPE)</a>. If the driver does support VPE, it should initialize and return a <a href="/windows/desktop/api/ddrawint/ns-ddrawint-dd_videoportcallbacks">DD_VIDEOPORTCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCaps

</td>
<td>
Queries whether the driver supports any of the VPE object capabilities specified through the <a href="/windows/desktop/api/dvp/ns-dvp-ddvideoportcaps">DDVIDEOPORTCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDVIDEOPORTCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_ZPixelFormats

</td>
<td>
Queries the pixel formats supported by the depth buffer. If the driver supports Direct3D, it should allocate and initialize the appropriate members of a DDPIXELFORMAT structure for every z-buffer format that it supports and return these in the buffer to which <b>lpvData</b> points.

</td>
</tr>
</table>

### -field dwExpectedSize

Specifies the number of bytes of data that DirectDraw expects the driver to pass back in the buffer to which <b>lpvData</b> points.

### -field lpvData

Points to a DirectDraw-allocated buffer into which the driver copies the requested data. This buffer is typically <b>dwExpectedSize</b> bytes in size. The driver must not write more than <b>dwExpectedSize</b> bytes of data in it. The driver specifies the number of bytes that it writes to this buffer in the <b>dwActualSize</b> member.

### -field dwActualSize

Specifies the location in which the driver returns the number of bytes of data it writes in <b>lpvData</b>.

### -field ddRVal

Specifies the location in which the driver writes the return value of the <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="/windows-hardware/drivers/display/return-values-for-directdraw">Return Values for DirectDraw</a>.

## -remarks

The data structure passed to the driver for a <a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a> call has minor differences between Windows 98/Me and Windows 2000 and later. On Windows 2000 and later the data structure is called DD_GETDRIVERINFODATA and on Windows 98/Me the data structure is called DDHAL_GETDRIVERINFODATA. Both data structures include a field for driver specific context information. On Windows 2000 and later, DD_GETDRIVERINFODATA includes a field <b>dhpdev</b> that stores the DHPDEV of the driver being called. Only on Windows 98/Me, DDHAL_GETDRIVERINFODATA includes a field <b>dwContext</b> that is copied for the driver reserved <b>dwReserved3</b> field of the DirectDraw global object.

## -see-also

<a href="/windows/desktop/api/ddrawint/nc-ddrawint-pdd_getdriverinfo">DdGetDriverInfo</a>