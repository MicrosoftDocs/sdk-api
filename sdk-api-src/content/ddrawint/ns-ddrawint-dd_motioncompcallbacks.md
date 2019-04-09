---
UID: NS:ddrawint.DD_MOTIONCOMPCALLBACKS
title: DD_MOTIONCOMPCALLBACKS (ddrawint.h)
author: windows-sdk-content
description: The DD_MOTIONCOMPCALLBACKS structure contains entry pointers to the motion compensation callback functions that a device driver supports.
old-location: display\dd_motioncompcallbacks.htm
tech.root: display
ms.assetid: db707fd8-2190-4c4f-89fd-ab46d97f66a2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PDD_MOTIONCOMPCALLBACKS, DD_MOTIONCOMPCALLBACKS, DD_MOTIONCOMPCALLBACKS structure [Display Devices], PDD_MOTIONCOMPCALLBACKS, PDD_MOTIONCOMPCALLBACKS structure pointer [Display Devices], ddrawint/DD_MOTIONCOMPCALLBACKS, ddrawint/PDD_MOTIONCOMPCALLBACKS, ddstrcts_b9c5a52b-5814-42ae-8002-0de8f7c0bca5.xml, display.dd_motioncompcallbacks"
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
 - DD_MOTIONCOMPCALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_MOTIONCOMPCALLBACKS
req.redist: 
---

# DD_MOTIONCOMPCALLBACKS structure


## -description


The DD_MOTIONCOMPCALLBACKS structure contains entry pointers to the motion compensation callback functions that a device driver supports.


## -struct-fields




### -field dwSize

Specifies the size in bytes of this DD_MOTIONCOMPCALLBACKS structure.


### -field dwFlags

Indicates what additional Microsoft DirectDraw motion compensation callback functions the driver has implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_MOCOMP32_BEGINFRAME</dt>
<dt>DDHAL_MOCOMP32_CREATE</dt>
<dt>DDHAL_MOCOMP32_DESTROY</dt>
<dt>DDHAL_MOCOMP32_GETCOMPBUFFINFO</dt>
<dt>DDHAL_MOCOMP32_GETINTERNALINFO</dt>
<dt>DDHAL_MOCOMP32_ENDFRAME</dt>
<dt>DDHAL_MOCOMP32_GETFORMATS</dt>
<dt>DDHAL_MOCOMP32_GETGUIDS</dt>
<dt>DDHAL_MOCOMP32_QUERYSTATUS</dt>
<dt>DDHAL_MOCOMP32_RENDER</dt>
</dl>



### -field GetMoCompGuids

Points to the driver-supplied <a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a> callback function.


### -field GetMoCompFormats

Points to the driver-supplied <a href="https://msdn.microsoft.com/9df6473f-32a1-49bd-9ddb-2f2adec3cb45">DdMoCompGetFormats</a> callback function.


### -field CreateMoComp

Points to the driver-supplied <a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a> callback function.


### -field GetMoCompBuffInfo

Points to the driver-supplied <a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a> callback function. 


### -field GetInternalMoCompInfo

Points to the driver-supplied <a href="https://msdn.microsoft.com/297ff4a2-52f4-4b24-9abe-9c7d22a9b3ad">DdMoCompGetInternalInfo</a> callback function.


### -field BeginMoCompFrame

Points to the driver-supplied <a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a> callback function.


### -field EndMoCompFrame

Points to the driver-supplied <a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a> callback function.


### -field RenderMoComp

Points to the driver-supplied <a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a> callback function.


### -field QueryMoCompStatus

Points to the driver-supplied <a href="https://msdn.microsoft.com/af62d169-665a-43d2-ac0c-cc8ce6ce42d0">DdMoCompQueryStatus</a> callback function.


### -field DestroyMoComp

Points to the driver-supplied <a href="https://msdn.microsoft.com/7a8900d0-4c9f-4600-8408-197f4e7c78ba">DdMoCompDestroy</a> callback function.


## -remarks



Entries that the display driver does not use should be set to <b>NULL</b>. The driver should initialize this structure when its <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> function is called with the GUID_MotionCompCallbacks GUID.




## -see-also




<a href="https://msdn.microsoft.com/fcf0e136-a7cc-4bb3-8af4-2478d4a2c055">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/85dcb71b-ad1f-4b83-8ead-db502d9f294e">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/9bf47408-cc7f-455d-bbb2-6f1f318eee5f">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/9d226b1c-6959-4cc8-9e60-b57a324d9a8a">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/742b03b0-f729-489c-a87f-b8eb404b6290">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/a363446e-a9f7-4b32-acc2-c369d3dfe8f3">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/5e03d240-f483-4ecf-8890-b9f0368e2b2f">DD_VIDEOPORTCALLBACKS</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>



<a href="https://msdn.microsoft.com/0038aedc-2e4f-4d89-878f-7f6f751015cc">DdMoCompBeginFrame</a>



<a href="https://msdn.microsoft.com/9413108b-f9b5-4d1c-83a9-b663a9f444bf">DdMoCompCreate</a>



<a href="https://msdn.microsoft.com/7a8900d0-4c9f-4600-8408-197f4e7c78ba">DdMoCompDestroy</a>



<a href="https://msdn.microsoft.com/3589f003-32fc-44c4-867a-abf54f347de9">DdMoCompEndFrame</a>



<a href="https://msdn.microsoft.com/7303f80d-1b6e-401f-a9ef-cf646b716c70">DdMoCompGetBuffInfo</a>



<a href="https://msdn.microsoft.com/9df6473f-32a1-49bd-9ddb-2f2adec3cb45">DdMoCompGetFormats</a>



<a href="https://msdn.microsoft.com/22c6a3f2-4a27-4a4b-a021-8f2be04e4f87">DdMoCompGetGuids</a>



<a href="https://msdn.microsoft.com/297ff4a2-52f4-4b24-9abe-9c7d22a9b3ad">DdMoCompGetInternalInfo</a>



<a href="https://msdn.microsoft.com/af62d169-665a-43d2-ac0c-cc8ce6ce42d0">DdMoCompQueryStatus</a>



<a href="https://msdn.microsoft.com/d88f2c7e-e3e5-4444-836c-a45d52c86e54">DdMoCompRender</a>
 

 

