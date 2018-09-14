---
UID: NS:ddrawint._DD_GETDRIVERINFODATA
title: "_DD_GETDRIVERINFODATA"
author: windows-sdk-content
description: The DD_GETDRIVERINFODATA structure is used to pass data to and from the DdGetDriverInfo callback routine.
old-location: display\dd_getdriverinfodata.htm
tech.root: display
ms.assetid: 15a4e80d-2186-4683-a05f-405ca75044e5
ms.author: windowssdkdev
ms.date: 09/13/2018
ms.keywords: "*PDD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA structure [Display Devices], PDD_GETDRIVERINFODATA, PDD_GETDRIVERINFODATA structure pointer [Display Devices], _DD_GETDRIVERINFODATA, ddrawint/DD_GETDRIVERINFODATA, ddrawint/PDD_GETDRIVERINFODATA, ddstrcts_1c0cf063-699e-497d-8554-db34185a1668.xml, display.dd_getdriverinfodata"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ddrawint.h
api_name:
 - DD_GETDRIVERINFODATA
product: Windows
targetos: Windows
req.typenames: "*PDD_GETDRIVERINFODATA, DD_GETDRIVERINFODATA"
req.redist: 
---

# _DD_GETDRIVERINFODATA structure


## -description


The DD_GETDRIVERINFODATA structure is used to pass data to and from the <i>DdGetDriverInfo</i> callback routine.


## -struct-fields




### -field dhpdev

Handle to the driver's <a href="https://msdn.microsoft.com/d3172dd2-ecf1-4ad8-ba52-776bf712ab7c">PDEV</a>. Microsoft Windows 2000 and later only.


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
Queries whether the driver supports <a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a>. If the driver does support it, the driver should initialize and return a <a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/3b045732-a41f-47e7-9835-41e3ef54f14c">D3DHAL_CALLBACKS</a> structure. If the driver does not provide any of this support, it should initialize and return a D3DHAL_CALLBACKS structure in the buffer to which <b>lpvData</b> points.

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
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/09215332-4ee3-4f7b-be25-091b8d85fd6b">D3DHAL_CALLBACKS3</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_CALLBACKS3 structure in the buffer to which <b>lpvData</b> points.

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
Queries whether the driver supports any of the Microsoft Direct3D functionality specified through the <a href="https://msdn.microsoft.com/b1e63dce-6d51-438c-a4aa-cc17d9292576">D3DHAL_D3DEXTENDEDCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_D3DEXTENDEDCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DParseUnknownCommandCallback

</td>
<td>
Provides the Direct3D portion of the driver with the Direct3D runtime's <i>D3dParseUnknownCommandCallback</i>. The driver's <a href="https://msdn.microsoft.com/6128ff7a-0d2c-48df-8b5e-cab33c5a74f5">D3dDrawPrimitives2</a> callback calls <i>D3dParseUnknownCommandCallback</i> to parse commands from the command buffer that the driver doesn't understand.DirectDraw passes a pointer to this function in the buffer to which <b>lpvData</b> points. If the driver supports this aspect of Direct3D, it should store the pointer.

</td>
</tr>
<tr>
<td>
GUID_GetHeapAlignment

</td>
<td>
Queries whether the driver supports surface alignment requirements on a per-heap basis. If the driver does provide this support, it should initialize and return a <a href="https://msdn.microsoft.com/5bdc13e3-396d-45f6-8c90-a831bbb23628">DD_GETHEAPALIGNMENTDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_KERNELCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCaps

</td>
<td>
Queries whether the driver supports any of the kernel-mode capabilities specified through the <a href="https://msdn.microsoft.com/d02d26f5-34cf-4a3c-b67c-0f9191bb854b">DDKERNELCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDKERNELCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MiscellaneousCallbacks

</td>
<td>
Queries whether the driver supports <a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a>. If the driver does support it, the driver should initialize and return a <a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_Miscellaneous2Callbacks

</td>
<td>
Queries whether the driver supports the additional miscellaneous functionality specified in the <a href="https://msdn.microsoft.com/bb3e91c0-5399-4760-a12e-0a47f0fbd2f9">DD_MISCELLANEOUS2CALLBACKS</a> structure. If the driver does support any of this support, the driver should initialize and return a DD_MISCELLANEOUS2CALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MotionCompCallbacks

</td>
<td>
Queries whether the driver supports the motion compensation functionality specified through the <a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a> structure. If the driver does provide any of this support, is should initialize and return a DD_MOTIONCOMPCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NonLocalVidMemCaps

</td>
<td>
Queries whether the driver supports any of the nonlocal display memory capabilities specified through the <a href="https://msdn.microsoft.com/1ccc7de7-e5a3-4dc0-9375-a54460d43936">DD_NONLOCALVIDMEMCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NONLOCALVIDMEMCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTPrivateDriverCaps

</td>
<td>
Queries whether the driver supports the Windows 98/Me-style surface creation techniques specified through the <a href="https://msdn.microsoft.com/d802b080-cf94-400a-96c4-e765008dfc8a">DD_NTPRIVATEDRIVERCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTPRIVATEDRIVERCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_UpdateNonLocalHeap

</td>
<td>
Queries whether the driver supports retrieval of the base addresses of each nonlocal heap in turn. If the driver does provide this support, it should initialize and return a <a href="https://msdn.microsoft.com/ef16df6f-dbc6-40ee-9c86-be9c3d132b28">DD_UPDATENONLOCALHEAPDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCallbacks

</td>
<td>
Queries whether the driver supports the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a>. If the driver does support VPE, it should initialize and return a <a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCaps

</td>
<td>
Queries whether the driver supports any of the VPE object capabilities specified through the <a href="https://msdn.microsoft.com/ea85f189-7308-48ad-b159-1809749f8183">DDVIDEOPORTCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDVIDEOPORTCAPS structure in the buffer to which <b>lpvData</b> points.

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

Specifies the location in which the driver writes the return value of the <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> callback. A return code of DD_OK indicates success. For more information, see <a href="https://msdn.microsoft.com/da4cc7d7-6826-48aa-96c6-004e31fc3e3e">Return Values for DirectDraw</a>.


## -remarks



The data structure passed to the driver for a <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> call has minor differences between Windows 98/Me and Windows 2000 and later. On Windows 2000 and later the data structure is called DD_GETDRIVERINFODATA and on Windows 98/Me the data structure is called DDHAL_GETDRIVERINFODATA. Both data structures include a field for driver specific context information. On Windows 2000 and later, DD_GETDRIVERINFODATA includes a field <b>dhpdev</b> that stores the DHPDEV of the driver being called. Only on Windows 98/Me, DDHAL_GETDRIVERINFODATA includes a field <b>dwContext</b> that is copied for the driver reserved <b>dwReserved3</b> field of the DirectDraw global object.




## -see-also




<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

