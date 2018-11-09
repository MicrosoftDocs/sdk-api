---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0013_0001
title: "__MIDL___MIDL_itf_vmr9_0000_0013_0001"
author: windows-sdk-content
description: The VMR9DeinterlacePrefs enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 9 (VMR-9) uses if the method set by the application cannot be used.
old-location: dshow\vmr9deinterlaceprefs.htm
tech.root: DirectShow
ms.assetid: 1e5f5749-bdf9-4220-9867-ba6899797850
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: DeinterlacePref9_BOB, DeinterlacePref9_Mask, DeinterlacePref9_NextBest, DeinterlacePref9_Weave, VMR9DeinterlacePrefs, VMR9DeinterlacePrefs , VMR9DeinterlacePrefs enumeration [DirectShow], VMR9DeinterlacePrefsEnumeration, __MIDL___MIDL_itf_vmr9_0000_0013_0001, dshow.vmr9deinterlaceprefs, vmr9/DeinterlacePref9_BOB, vmr9/DeinterlacePref9_Mask, vmr9/DeinterlacePref9_NextBest, vmr9/DeinterlacePref9_Weave, vmr9/VMR9DeinterlacePrefs
ms.prod: windows
ms.technology: windows-sdk
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
 - VMR9DeinterlacePrefs
product: Windows
targetos: Windows
req.typenames: VMR9DeinterlacePrefs
req.redist: 
---

# __MIDL___MIDL_itf_vmr9_0000_0013_0001 enumeration


## -description



The <code>VMR9DeinterlacePrefs</code> enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 9 (VMR-9) uses if the method set by the application cannot be used.




## -enum-fields




### -field DeinterlacePref9_NextBest

Use the next best mode offered by the driver.


### -field DeinterlacePref9_BOB

Use the bob method.


### -field DeinterlacePref9_Weave

Use the weave method (that is, no deinterlacing).


### -field DeinterlacePref9_Mask

Bitwise OR of the previous flags. This value is used internally by the VMR, and is not a valid flag.


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/685f3627-30bd-4c78-9eda-0b06203dd46e">IVMRDeinterlaceControl9 Interface</a>
 

 

