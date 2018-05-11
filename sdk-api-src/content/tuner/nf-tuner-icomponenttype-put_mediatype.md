---
UID: NF:tuner.IComponentType.put_MediaType
title: IComponentType::put_MediaType
author: windows-driver-content
description: The put_MediaType method sets the DirectShow AM_MEDIA_TYPE structure for the component.
old-location: mstv\icomponenttype_put_mediatype.htm
old-project: mstv
ms.assetid: 6f77a391-232f-46ef-a028-763ebc706784
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaType method, IComponentType.put_MediaType, IComponentType::put_MediaType, IComponentTypeput_MediaType, mstv.icomponenttype_put_mediatype, put_MediaType, put_MediaType method [Microsoft TV Technologies], put_MediaType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaType
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
-	IComponentType.put_MediaType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::put_MediaType


## -description



The <b>put_MediaType</b> method sets the DirectShow <b>AM_MEDIA_TYPE</b> structure for the component.




## -parameters




### -param MediaType [in]


              An <a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a> structure that specifies the major type, subtype, format, and so on.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 

