---
UID: NS:mfobjects._MFVideoArea
title: "_MFVideoArea"
author: windows-driver-content
description: Specifies a rectangular area within a video frame.
old-location: mf\mfvideoarea.htm
old-project: medfound
ms.assetid: d22b8b9c-399b-4fce-a173-833005b5bf03
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: MFVideoArea, MFVideoArea structure [Media Foundation], _MFVideoArea, d22b8b9c-399b-4fce-a173-833005b5bf03, mf.mfvideoarea, mfobjects/MFVideoArea
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: mfobjects.h
req.include-header: Mfidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MFVideoArea
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	mfobjects.h
api_name:
-	MFVideoArea
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _MFVideoArea structure


## -description



          Specifies a rectangular area within a video frame.
        


## -struct-fields




### -field OffsetX


              An <a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a> structure that contains the x-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field OffsetY


              An <a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a> structure that contains the y-coordinate of the upper-left corner of the rectangle. This coordinate might have a fractional value.
          


### -field Area


              A <a href="https://msdn.microsoft.com/library/windows/hardware/dn915850">SIZE</a> structure that contains the width and height of the rectangle.
          


## -see-also




<a href="https://msdn.microsoft.com/e93539fe-3e4a-4b34-8d6a-b3f300a70ffc">MFOffset</a>



<a href="https://msdn.microsoft.com/39fdd724-13ca-48ab-8a55-93529d1da3b4">Media Foundation Structures</a>
 

 

