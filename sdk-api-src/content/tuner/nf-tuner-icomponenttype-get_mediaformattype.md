---
UID: NF:tuner.IComponentType.get_MediaFormatType
title: IComponentType::get_MediaFormatType method
author: windows-driver-content
description: The get_MediaFormatType method retrieves the DirectShow media format type as a BSTR.
old-location: mstv\icomponenttype_get_mediaformattype.htm
old-project: mstv
ms.assetid: 5b618f33-2ef8-420b-9a15-83e1899476bc
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: IComponentType, IComponentType interface [Microsoft TV Technologies], get_MediaFormatType method, IComponentType::get_MediaFormatType, IComponentTypeget_MediaFormatType, get_MediaFormatType method [Microsoft TV Technologies], get_MediaFormatType method [Microsoft TV Technologies], IComponentType interface, get_MediaFormatType,IComponentType.get_MediaFormatType, mstv.icomponenttype_get_mediaformattype, tuner/IComponentType::get_MediaFormatType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tuner.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Tuner.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: BITMAP_RENDERER_STATISTICS, *PBITMAP_RENDERER_STATISTICS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	tuner.h
api_name:
-	IComponentType.get_MediaFormatType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::get_MediaFormatType method


## -description



The <b>get_MediaFormatType</b> method retrieves the DirectShow media format type as a <b>BSTR</b>.




## -parameters




### -param MediaFormatType






#### - pMediaFormatType [out]

Pointer to a <b>BSTR</b> that will receive the GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 

