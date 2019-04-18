---
UID: NE:vmr9.__MIDL___MIDL_itf_vmr9_0000_0000_0002
title: VMR9PresentationFlags (vmr9.h)
author: windows-sdk-content
description: The VMR9PresentationFlags enumeration type contains flags that describe the status of a video sample. These flags are used in the VMR9PresentationInfo structure.
old-location: dshow\vmr9presentationflags.htm
tech.root: DirectShow
ms.assetid: 97db420f-a6a5-4c87-9c7f-9733a1ce2b46
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: VMR9PresentationFlags, VMR9PresentationFlags , VMR9PresentationFlags enumeration [DirectShow], VMR9PresentationFlagsEnumeration, VMR9Sample_Discontinuity, VMR9Sample_Preroll, VMR9Sample_SyncPoint, VMR9Sample_TimeValid, dshow.vmr9presentationflags, enumeration [DirectShow], vmr9/VMR9PresentationFlags, vmr9/VMR9Sample_Discontinuity, vmr9/VMR9Sample_Preroll, vmr9/VMR9Sample_SyncPoint, vmr9/VMR9Sample_TimeValid
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
 - VMR9PresentationFlags
product: Windows
targetos: Windows
req.typenames: VMR9PresentationFlags
req.redist: 
ms.custom: 19H1
---

# VMR9PresentationFlags enumeration


## -description



The <code>VMR9PresentationFlags</code> enumeration type contains flags that describe the status of a video sample. These flags are used in the <a href="https://msdn.microsoft.com/en-us/library/Dd407371(v=VS.85).aspx">VMR9PresentationInfo</a> structure.




## -enum-fields




### -field VMR9Sample_SyncPoint

Indicates that the sample is a sync point.


### -field VMR9Sample_Preroll

Indicates that the sample is part of the preroll.


### -field VMR9Sample_Discontinuity

Indicates that the sample is a discontinuity.


### -field VMR9Sample_TimeValid

Indicates that the time stamp on the sample is valid.


### -field VMR9Sample_SrcDstRectsValid




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

