---
UID: NF:dvbsiparser.IDvbParentalRatingDescriptor.GetTag
title: IDvbParentalRatingDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that describes a Digital Video Broadcast (DVB) parental rating descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbParentalRatingDescriptor interface","IDvbParentalRatingDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbParentalRatingDescriptor.GetTag","IDvbParentalRatingDescriptor::GetTag","dvbsiparser/IDvbParentalRatingDescriptor::GetTag","mstv.idvbparentalratingdescriptor_gettag"]
old-location: mstv\idvbparentalratingdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 30689876-39be-44dd-a480-c660dcf3ddd1
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbParentalRatingDescriptor interface, IDvbParentalRatingDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbParentalRatingDescriptor.GetTag, IDvbParentalRatingDescriptor::GetTag, dvbsiparser/IDvbParentalRatingDescriptor::GetTag, mstv.idvbparentalratingdescriptor_gettag
f1_keywords:
- dvbsiparser/IDvbParentalRatingDescriptor.GetTag
dev_langs:
- c++
req.header: dvbsiparser.h
req.include-header: Dvbsiparser.idl
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
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
- dvbsiparser.h
api_name:
- IDvbParentalRatingDescriptor.GetTag
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDvbParentalRatingDescriptor::GetTag


## -description


 Gets the tag that describes a Digital Video Broadcast (DVB) parental rating descriptor.


## -parameters




### -param pbVal [out]

Receives the parental rating descriptor tag. This value is "0x55" for parental rating descriptors.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbparentalratingdescriptor">IDvbParentalRatingDescriptor</a>
 

 

