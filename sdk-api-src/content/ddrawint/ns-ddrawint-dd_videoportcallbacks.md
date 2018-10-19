---
UID: NS:ddrawint.DD_VIDEOPORTCALLBACKS
title: DD_VIDEOPORTCALLBACKS
author: windows-sdk-content
description: The DD_VIDEOPORTCALLBACKS structure contains entry pointers to Microsoft DirectDraw video port extensions (VPE) callback functions that a device driver supports.
old-location: display\dd_videoportcallbacks.htm
tech.root: display
ms.assetid: 5e03d240-f483-4ecf-8890-b9f0368e2b2f
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: "*PDD_VIDEOPORTCALLBACKS, DD_VIDEOPORTCALLBACKS, DD_VIDEOPORTCALLBACKS structure [Display Devices], PDD_VIDEOPORTCALLBACKS, PDD_VIDEOPORTCALLBACKS structure pointer [Display Devices], ddrawint/DD_VIDEOPORTCALLBACKS, ddrawint/PDD_VIDEOPORTCALLBACKS, ddstrcts_e0a55748-eb24-4e5f-8208-bcb0083cdf21.xml, display.dd_videoportcallbacks"
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
 - DD_VIDEOPORTCALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_VIDEOPORTCALLBACKS
req.redist: 
---

# DD_VIDEOPORTCALLBACKS structure


## -description


The DD_VIDEOPORTCALLBACKS structure contains entry pointers to Microsoft DirectDraw <a href="https://msdn.microsoft.com/a1de1905-09f3-4689-ace9-06690a1f930a">video port extensions (VPE)</a> callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_VIDEOPORTCALLBACKS structure.


### -field dwFlags

Indicates what VPE callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_VPORT32_CANCREATEVIDEOPORT</dt>
<dt>DDHAL_VPORT32_CREATEVIDEOPORT</dt>
<dt>DDHAL_VPORT32_FLIP</dt>
<dt>DDHAL_VPORT32_GETBANDWIDTH</dt>
<dt>DDHAL_VPORT32_GETINPUTFORMATS</dt>
<dt>DDHAL_VPORT32_GETOUTPUTFORMATS</dt>
<dt>DDHAL_VPORT32_GETAUTOFLIPSURF</dt>
<dt>DDHAL_VPORT32_GETFIELD</dt>
<dt>DDHAL_VPORT32_GETLINE</dt>
<dt>DDHAL_VPORT32_GETCONNECT</dt>
<dt>DDHAL_VPORT32_DESTROY</dt>
<dt>DDHAL_VPORT32_GETFLIPSTATUS</dt>
<dt>DDHAL_VPORT32_UPDATE</dt>
<dt>DDHAL_VPORT32_WAITFORSYNC</dt>
<dt>DDHAL_VPORT32_GETSIGNALSTATUS</dt>
<dt>DDHAL_VPORT32_COLORCONTROL</dt>
</dl>



### -field CanCreateVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/742c7af2-0611-4cca-b18c-e14b18068d7e">DdVideoPortCanCreate</a> callback.


### -field CreateVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/eeaf3cda-6220-4e8e-8f9e-9f52d1b05ab7">DdVideoPortCreate</a> callback.


### -field FlipVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/1e31f33d-84da-40fa-a43c-30ad7d3055e8">DdVideoPortFlip</a> callback.


### -field GetVideoPortBandwidth

Points to the driver-supplied <a href="https://msdn.microsoft.com/4b9cfec1-a599-47a5-878e-2cde6b3b780a">DdVideoPortGetBandwidth</a> callback.


### -field GetVideoPortInputFormats

Points to the driver-supplied <a href="https://msdn.microsoft.com/aac34116-a6a2-4d00-b0c4-87fac786b68d">DdVideoPortGetInputFormats</a> callback.


### -field GetVideoPortOutputFormats

Points to the driver-supplied <a href="https://msdn.microsoft.com/8e9df88b-a50a-4838-9732-9f818936cbcb">DdVideoPortGetOutputFormats</a> callback.


### -field lpReserved1

Reserved for system use and should be ignored by the driver.


### -field GetVideoPortField

Points to the driver-supplied <a href="https://msdn.microsoft.com/e8c99103-31cd-4468-8b6b-1e56b31e10da">DdVideoPortGetField</a> callback.


### -field GetVideoPortLine

Points to the driver-supplied <a href="https://msdn.microsoft.com/6c0cfa87-bc16-47a6-8106-e5a1b1456813">DdVideoPortGetLine</a> callback.


### -field GetVideoPortConnectInfo

Points to the driver-supplied <a href="https://msdn.microsoft.com/b6be5f94-6d4d-4f7a-a8d9-15bfc7a15d3b">DdVideoPortGetConnectInfo</a> callback.


### -field DestroyVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/0426eeaa-4d9a-4e5e-8550-2f7adbb26685">DdVideoPortDestroy</a> callback.


### -field GetVideoPortFlipStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/67a7aa80-2201-4bb7-919b-dd9ca1228f06">DdVideoPortGetFlipStatus</a> callback.


### -field UpdateVideoPort

Points to the driver-supplied <a href="https://msdn.microsoft.com/50a55a89-bae0-4a65-96ef-3e9903f45a0c">DdVideoPortUpdate</a> callback.


### -field WaitForVideoPortSync

Points to the driver-supplied <a href="https://msdn.microsoft.com/0834f49b-89c4-47cc-b591-d2b90d21ee72">DdVideoPortWaitForSync</a> callback.


### -field GetVideoSignalStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/d3868acf-b119-4ab3-aa85-64d50f76fdb7">DdVideoPortGetSignalStatus</a> callback.


### -field ColorControl

Points to the driver-supplied <a href="https://msdn.microsoft.com/0d4d5157-cadf-4b63-aafc-ccb252cec2b4">DdVideoPortColorControl</a> callback.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_VideoPortCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/db707fd8-2190-4c4f-89fd-ab46d97f66a2">DD_MOTIONCOMPCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

