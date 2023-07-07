---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetTag
title: IDvbContentDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag for a Digital Video Broadcast (DVB) content descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbContentDescriptor interface","IDvbContentDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbContentDescriptor.GetTag","IDvbContentDescriptor::GetTag","dvbsiparser/IDvbContentDescriptor::GetTag","mstv.idvbcontentdescriptor_gettag"]
old-location: mstv\idvbcontentdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 3cfbda01-ef69-4b69-90f4-04dd3044ae1f
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbContentDescriptor.GetTag, IDvbContentDescriptor::GetTag, dvbsiparser/IDvbContentDescriptor::GetTag, mstv.idvbcontentdescriptor_gettag
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDvbContentDescriptor::GetTag
 - dvbsiparser/IDvbContentDescriptor::GetTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - dvbsiparser.h
api_name:
 - IDvbContentDescriptor.GetTag
---

# IDvbContentDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag for a Digital Video Broadcast (DVB) content descriptor.

## -parameters

### -param pbVal [out]

Receives the content descriptor tag. For content descriptors, this tag value is "0x54".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentdescriptor">IDvbContentDescriptor</a>