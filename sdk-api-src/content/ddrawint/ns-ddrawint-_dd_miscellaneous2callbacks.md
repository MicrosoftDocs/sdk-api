---
UID: NS:ddrawint._DD_MISCELLANEOUS2CALLBACKS
title: "_DD_MISCELLANEOUS2CALLBACKS"
author: windows-sdk-content
description: The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines.
old-location: display\dd_miscellaneous2callbacks.htm
tech.root: display
ms.assetid: bb3e91c0-5399-4760-a12e-0a47f0fbd2f9
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: "*PDD_MISCELLANEOUS2CALLBACKS, DD_MISCELLANEOUS2CALLBACKS, DD_MISCELLANEOUS2CALLBACKS structure [Display Devices], PDD_MISCELLANEOUS2CALLBACKS, PDD_MISCELLANEOUS2CALLBACKS structure pointer [Display Devices], _DD_MISCELLANEOUS2CALLBACKS, ddrawint/DD_MISCELLANEOUS2CALLBACKS, ddrawint/PDD_MISCELLANEOUS2CALLBACKS, ddstrcts_61459de1-283c-4693-a27a-f5dc8bdc5a44.xml, display.dd_miscellaneous2callbacks"
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
 - DD_MISCELLANEOUS2CALLBACKS
product: Windows
targetos: Windows
req.typenames: DD_MISCELLANEOUS2CALLBACKS, *PDD_MISCELLANEOUS2CALLBACKS
req.redist: 
---

# _DD_MISCELLANEOUS2CALLBACKS structure


## -description


The DD_MISCELLANEOUS2CALLBACKS structure is used to return the addresses of miscellaneous callback routines. These routines are new for Microsoft DirectX 7.0 and later and are exposed through <a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a> by responding to the GUID_Miscellaneous2Callbacks GUID.


## -struct-fields




### -field dwSize

Specifies the size, in bytes, of this structure.


### -field dwFlags

Indicates which miscellaneous callback functions the driver implemented. For every bit set in <b>dwFlags</b>, the driver must initialize the corresponding function pointer member of this structure. This member can be one or more of the following flags:


<dl>
<dt>DDHAL_MISC2CB32_CREATESURFACEEX</dt>
<dt>DDHAL_MISC2CB32_GETDRIVERSTATE</dt>
<dt>DDHAL_MISC2CB32_DESTROYDDLOCAL</dt>
</dl>



### -field AlphaBlt

Unused and must be set to <b>NULL</b>. 


### -field CreateSurfaceEx

Points to the driver's <a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a> implementation. This callback creates an association between a DirectDraw surface and a small integer handle. 


### -field GetDriverState

Points to the driver's <a href="https://msdn.microsoft.com/6e1b0bce-1ac5-46e7-ae25-b0d3ce8580a0">D3dGetDriverState</a> implementation. 


### -field DestroyDDLocal

Points to the driver's <a href="https://msdn.microsoft.com/c68b924b-422d-4a01-8dac-674835833798">D3dDestroyDDLocal</a> implementation. Used to destroy the local copy of the device context. 


## -see-also




<a href="https://msdn.microsoft.com/dd07e49c-ec1f-4ba6-8b17-80ce6d3c5813">D3dCreateSurfaceEx</a>



<a href="https://msdn.microsoft.com/c68b924b-422d-4a01-8dac-674835833798">D3dDestroyDDLocal</a>



<a href="https://msdn.microsoft.com/6e1b0bce-1ac5-46e7-ae25-b0d3ce8580a0">D3dGetDriverState</a>



<a href="https://msdn.microsoft.com/89a22163-a678-4c72-932a-ae4d17922e0b">DdGetDriverInfo</a>
 

 

