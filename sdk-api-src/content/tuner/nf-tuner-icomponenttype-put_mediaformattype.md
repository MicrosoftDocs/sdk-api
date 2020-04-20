---
UID: NF:tuner.IComponentType.put_MediaFormatType
title: IComponentType::put_MediaFormatType (tuner.h)
description: The put_MediaFormatType method sets the DirectShow media format type.helpviewer_keywords: ["IComponentType interface [Microsoft TV Technologies]","put_MediaFormatType method","IComponentType.put_MediaFormatType","IComponentType::put_MediaFormatType","IComponentTypeput_MediaFormatType","mstv.icomponenttype_put_mediaformattype","put_MediaFormatType","put_MediaFormatType method [Microsoft TV Technologies]","put_MediaFormatType method [Microsoft TV Technologies]","IComponentType interface","tuner/IComponentType::put_MediaFormatType"]
old-location: mstv\icomponenttype_put_mediaformattype.htm
tech.root: mstv
ms.assetid: cfbf49a1-473b-4b51-ac35-a9ea982dcd7f
ms.date: 12/05/2018
ms.keywords: IComponentType interface [Microsoft TV Technologies],put_MediaFormatType method, IComponentType.put_MediaFormatType, IComponentType::put_MediaFormatType, IComponentTypeput_MediaFormatType, mstv.icomponenttype_put_mediaformattype, put_MediaFormatType, put_MediaFormatType method [Microsoft TV Technologies], put_MediaFormatType method [Microsoft TV Technologies],IComponentType interface, tuner/IComponentType::put_MediaFormatType
f1_keywords:
- tuner/IComponentType.put_MediaFormatType
dev_langs:
- c++
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- tuner.h
api_name:
- IComponentType.put_MediaFormatType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IComponentType::put_MediaFormatType


## -description



The <b>put_MediaFormatType</b> method sets the DirectShow media format type.




## -parameters




### -param MediaFormatType [in]

<b>BSTR</b> that specifies the GUID.


## -returns



Returns S_OK if successful. If the method fails, error information can be retrieved using the standard COM <b>IErrorInfo</b> interface.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/strmif/ns-strmif-am_media_type">AM_MEDIA_TYPE</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/tuner/nn-tuner-icomponenttype">IComponentType Interface</a>
 

 

