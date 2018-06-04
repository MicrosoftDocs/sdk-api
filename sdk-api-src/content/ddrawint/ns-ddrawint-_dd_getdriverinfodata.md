---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
Queries whether the driver supports <a href="https://msdn.microsoft.com/626fdd37-bebb-47b7-9899-7cf0dc2bd1ba">DdControlColor</a>. If the driver does support it, the driver should initialize and return a <a href="https://msdn.microsoft.com/library/windows/hardware/ff550521">DD_COLORCONTROLCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_D3DCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544716">D3DHAL_CALLBACKS</a> structure. If the driver does not provide any of this support, it should initialize and return a D3DHAL_CALLBACKS structure in the buffer to which <b>lpvData</b> points.

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
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544723">D3DHAL_CALLBACKS3</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_CALLBACKS3 structure in the buffer to which <b>lpvData</b> points.

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
Queries whether the driver supports any of the Microsoft Direct3D functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff544753">D3DHAL_D3DEXTENDEDCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a D3DHAL_D3DEXTENDEDCAPS structure in the buffer to which <b>lpvData</b> points.

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
Queries whether the driver supports surface alignment requirements on a per-heap basis. If the driver does provide this support, it should initialize and return a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551572">DD_GETHEAPALIGNMENTDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551633">DD_KERNELCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_KERNELCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_KernelCaps

</td>
<td>
Queries whether the driver supports any of the kernel-mode capabilities specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff549593">DDKERNELCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDKERNELCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MiscellaneousCallbacks

</td>
<td>
Queries whether the driver supports <a href="https://msdn.microsoft.com/21a1988a-1bfd-47b8-b4b6-1bc137b2ba64">DdGetAvailDriverMemory</a>. If the driver does support it, the driver should initialize and return a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551657">DD_MISCELLANEOUSCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_Miscellaneous2Callbacks

</td>
<td>
Queries whether the driver supports the additional miscellaneous functionality specified in the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551645">DD_MISCELLANEOUS2CALLBACKS</a> structure. If the driver does support any of this support, the driver should initialize and return a DD_MISCELLANEOUS2CALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_MotionCompCallbacks

</td>
<td>
Queries whether the driver supports the motion compensation functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551660">DD_MOTIONCOMPCALLBACKS</a> structure. If the driver does provide any of this support, is should initialize and return a DD_MOTIONCOMPCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NonLocalVidMemCaps

</td>
<td>
Queries whether the driver supports any of the nonlocal display memory capabilities specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551669">DD_NONLOCALVIDMEMCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NONLOCALVIDMEMCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTCallbacks

</td>
<td>
Queries whether the driver supports any of the functionality specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTCALLBACKS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_NTPrivateDriverCaps

</td>
<td>
Queries whether the driver supports the Windows 98/Me-style surface creation techniques specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff551676">DD_NTPRIVATEDRIVERCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DD_NTPRIVATEDRIVERCAPS structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_UpdateNonLocalHeap

</td>
<td>
Queries whether the driver supports retrieval of the base addresses of each nonlocal heap in turn. If the driver does provide this support, it should initialize and return a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551748">DD_UPDATENONLOCALHEAPDATA</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCallbacks

</td>
<td>
Queries whether the driver supports the <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a>. If the driver does support VPE, it should initialize and return a <a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a> structure in the buffer to which <b>lpvData</b> points.

</td>
</tr>
<tr>
<td>
GUID_VideoPortCaps

</td>
<td>
Queries whether the driver supports any of the VPE object capabilities specified through the <a href="https://msdn.microsoft.com/library/windows/hardware/ff550376">DDVIDEOPORTCAPS</a> structure. If the driver does provide any of this support, it should initialize and return a DDVIDEOPORTCAPS structure in the buffer to which <b>lpvData</b> points.

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
 

 

