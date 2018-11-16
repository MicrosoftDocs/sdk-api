---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0004_0001
title: "__MIDL___MIDL_itf_vmr9_0000_0004_0001"
author: windows-sdk-content
description: The VMR9AspectRatioMode enumeration type is used with the IVMRWindowlessControl9::GetAspectRatioMode and IVMRWindowlessControl9::SetAspectRatioMode methods to set and retrieve the aspect ratio mode (VMR-9 only).
old-location: dshow\vmr9aspectratiomode.htm
tech.root: DirectShow
ms.assetid: 745e7aad-a598-4be6-b28b-bb5969ef0c77
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: VMR9ARMode_LetterBox, VMR9ARMode_None, VMR9AspectRatioMode, VMR9AspectRatioMode , VMR9AspectRatioMode enumeration [DirectShow], VMR9AspectRatioModeEnumeration, __MIDL___MIDL_itf_vmr9_0000_0004_0001, dshow.vmr9aspectratiomode, vmr9/VMR9ARMode_LetterBox, vmr9/VMR9ARMode_None, vmr9/VMR9AspectRatioMode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: vmr9.h
req.include-header: 
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
 - Vmr9.h
api_name:
 - VMR9AspectRatioMode
product: Windows
targetos: Windows
req.typenames: VMR9AspectRatioMode
req.redist: 
---

# __MIDL___MIDL_itf_vmr9_0000_0004_0001 enumeration


## -description



The <code>VMR9AspectRatioMode</code> enumeration type is used with the <a href="https://msdn.microsoft.com/c18ab567-5e0d-400a-8dc1-e9ad83650b7c">IVMRWindowlessControl9::GetAspectRatioMode</a> and <a href="https://msdn.microsoft.com/5ba46490-0a82-495f-8742-d7a8efa95332">IVMRWindowlessControl9::SetAspectRatioMode</a> methods to set and retrieve the aspect ratio mode (VMR-9 only).




## -enum-fields




### -field VMR9ARMode_None

Indicates that the VMR is not attempting to maintain the aspect ratio of the source video.


### -field VMR9ARMode_LetterBox

Indicates that the VMR will maintain the aspect ratio of the source video by letterboxing within the output rectangle.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

