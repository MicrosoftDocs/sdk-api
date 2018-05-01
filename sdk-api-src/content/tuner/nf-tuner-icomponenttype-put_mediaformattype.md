---
UID: NF:tuner.IComponentType.put_MediaFormatType
title: IComponentType::put_MediaFormatType method
author: windows-driver-content
description: The put_MediaFormatType method sets the DirectShow media format type.
old-location: mstv\icomponenttype_put_mediaformattype.htm
old-project: mstv
ms.assetid: cfbf49a1-473b-4b51-ac35-a9ea982dcd7f
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IComponentType, IComponentType interface [Microsoft TV Technologies], put_MediaFormatType method, IComponentType::put_MediaFormatType, IComponentTypeput_MediaFormatType, mstv.icomponenttype_put_mediaformattype, put_MediaFormatType method [Microsoft TV Technologies], put_MediaFormatType method [Microsoft TV Technologies], IComponentType interface, put_MediaFormatType,IComponentType.put_MediaFormatType, tuner/IComponentType::put_MediaFormatType
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
-	IComponentType.put_MediaFormatType
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# IComponentType::put_MediaFormatType method


## -description



The <b>put_MediaFormatType</b> method sets the DirectShow media format type.




## -parameters




### -param MediaFormatType [in]

<b>BSTR</b> that specifies the GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://msdn.microsoft.com/973697d0-2897-48b5-88ca-a88a9650eb02">AM_MEDIA_TYPE</a>



<a href="https://msdn.microsoft.com/e83bbbbe-64a9-4ed3-9c32-925ca80c2c38">IComponentType Interface</a>
 

 

