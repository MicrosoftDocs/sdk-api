---
UID: NE:strmif.VMRDeinterlacePrefs
title: VMRDeinterlacePrefs (strmif.h)
author: windows-sdk-content
description: The VMRDeinterlacePrefs enumeration type describes the deinterlacing method that the Video Mixing Renderer Filter 7 (VMR-7) uses if the method set by the application cannot be used.
old-location: dshow\vmrdeinterlaceprefs.htm
tech.root: DirectShow
ms.assetid: 3f88abac-fc57-4f31-9a4c-cf0f7317d6f8
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: DeinterlacePref_BOB, DeinterlacePref_Mask, DeinterlacePref_NextBest, DeinterlacePref_Weave, VMRDeinterlacePrefs, VMRDeinterlacePrefs enumeration [DirectShow], VMRDeinterlacePrefsEnumeration, dshow.vmrdeinterlaceprefs, strmif/DeinterlacePref_BOB, strmif/DeinterlacePref_Mask, strmif/DeinterlacePref_NextBest, strmif/DeinterlacePref_Weave, strmif/VMRDeinterlacePrefs
ms.topic: enum
req.header: strmif.h
req.include-header: Dshow.h
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
 - strmif.h
api_name:
 - VMRDeinterlacePrefs
product: Windows
targetos: Windows
req.typenames: VMRDeinterlacePrefs
req.redist: 
req.product: Windows XP with SP1
---

# VMRDeinterlacePrefs enumeration


## -description


The <b>VMRDeinterlacePrefs</b> enumeration type describes the deinterlacing method that the <a href="https://msdn.microsoft.com/c83e6c50-76f2-4aeb-944b-5b244c6bf776">Video Mixing Renderer Filter 7</a> (VMR-7) uses if the method set by the application cannot be used.


## -enum-fields




### -field DeinterlacePref_NextBest

Use the next best mode offered by the driver.
          


### -field DeinterlacePref_BOB

Use the bob method.
          


### -field DeinterlacePref_Weave

Use the weave method (that is, no deinterlacing).
          


### -field DeinterlacePref_Mask

Bitwise <b>OR</b> of the previous flags. This value is not a valid flag.
          


## -see-also




<a href="https://msdn.microsoft.com/74467006-b077-49c0-8573-f939ac3d3444">DirectShow Enumerated Types</a>



<a href="https://msdn.microsoft.com/77abbcd4-6538-491d-b3c2-6a29a391c68a">IVMRDeinterlaceControl Interface</a>
 

 

