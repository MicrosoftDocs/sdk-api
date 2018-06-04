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




<a href="https://msdn.microsoft.com/library/windows/hardware/ff550521">DD_COLORCONTROLCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551633">DD_KERNELCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551657">DD_MISCELLANEOUSCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551673">DD_NTCALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551681">DD_PALETTECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551721">DD_SURFACECALLBACKS</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff551758">DD_VIDEOPORTCALLBACKS</a>



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
 

 

