---
UID: NE:strmif.VMRPresentationFlags
title: VMRPresentationFlags
author: windows-sdk-content
description: The VMRPresentationFlags enumeration type is a member of the VMRPRESENTATIONINFO structure .
old-location: dshow\vmrpresentationflags.htm
old-project: DirectShow
ms.assetid: 27aab657-802e-4967-a5bd-3907637e1cfe
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: VMRPresentationFlags, VMRPresentationFlags enumeration [DirectShow], VMRPresentationFlagsEnumeration, VMRSample_Discontinuity, VMRSample_Preroll, VMRSample_SyncPoint, VMRSample_TimeValid, dshow.vmrpresentationflags, strmif/VMRPresentationFlags, strmif/VMRSample_Discontinuity, strmif/VMRSample_Preroll, strmif/VMRSample_SyncPoint, strmif/VMRSample_TimeValid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VMRPresentationFlags
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - strmif.h
api_name:
 - VMRPresentationFlags
product: Windows
targetos: Windows
req.lib: Kernel32.lib
req.dll: Kernel32.dll
req.irql: 
req.product: Windows XP with SP1
---

# VMRPresentationFlags enumeration


## -description



The <b>VMRPresentationFlags</b> enumeration type is a member of the <a href="https://msdn.microsoft.com/cddbe3de-c5e2-4161-801f-f3497714922c">VMRPRESENTATIONINFO</a> structure .




## -enum-fields




### -field VMRSample_SyncPoint

Indicates that the sample is a sync point.
          


### -field VMRSample_Preroll

Indicates that the sample is part of the preroll.
          


### -field VMRSample_Discontinuity

Indicates that the sample is a discontinuity.
          


### -field VMRSample_TimeValid

Indicates that the time stamp on the sample is valid.
          


### -field VMRSample_SrcDstRectsValid




## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>
 

 

