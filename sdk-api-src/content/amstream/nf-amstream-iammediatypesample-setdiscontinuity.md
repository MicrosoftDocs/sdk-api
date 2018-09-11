---
UID: NF:amstream.IAMMediaTypeSample.SetDiscontinuity
title: IAMMediaTypeSample::SetDiscontinuity
author: windows-sdk-content
description: Note  This interface is deprecated. New applications should not use it. The SetDiscontinuity method sets the discontinuity property.
old-location: dshow\iammediatypesample_setdiscontinuity.htm
tech.root: DirectShow
ms.assetid: 9dcac2ce-c9a0-40be-aa86-b4acbd4d06a7
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: IAMMediaTypeSample interface [DirectShow],SetDiscontinuity method, IAMMediaTypeSample.SetDiscontinuity, IAMMediaTypeSample::SetDiscontinuity, IAMMediaTypeSampleSetDiscontinuity, SetDiscontinuity, SetDiscontinuity method [DirectShow], SetDiscontinuity method [DirectShow],IAMMediaTypeSample interface, amstream/IAMMediaTypeSample::SetDiscontinuity, dshow.iammediatypesample_setdiscontinuity
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: amstream.h
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
 - COM
api_location:
 - amstream.h
api_name:
 - IAMMediaTypeSample.SetDiscontinuity
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IAMMediaTypeSample::SetDiscontinuity


## -description



<div class="alert"><b>Note</b>  This interface is deprecated. New applications should not use it.</div>
<div> </div>
The <code>SetDiscontinuity</code> method sets the discontinuity property.




## -parameters




### -param bDiscontinuity

Value that specifies whether this sample is a discontinuity. If the sample is discontinuous with the previous sample, set the value to <b>TRUE</b>. Otherwise, set the value to <b>FALSE</b>.


## -returns



Returns S_OK.




## -see-also




<a href="https://msdn.microsoft.com/e0a62251-68ee-4318-b09a-0aac6b73bf54">IAMMediaTypeSample Interface</a>
 

 

