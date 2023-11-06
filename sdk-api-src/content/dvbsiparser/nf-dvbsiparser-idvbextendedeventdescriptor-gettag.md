---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetTag
title: IDvbExtendedEventDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbExtendedEventDescriptor.GetTag","IDvbExtendedEventDescriptor::GetTag","dvbsiparser/IDvbExtendedEventDescriptor::GetTag","mstv.idvbextendedeventdescriptor_gettag"]
old-location: mstv\idvbextendedeventdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 8f6dad8a-fd95-48c3-9bb2-222c5ec958f5
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbExtendedEventDescriptor.GetTag, IDvbExtendedEventDescriptor::GetTag, dvbsiparser/IDvbExtendedEventDescriptor::GetTag, mstv.idvbextendedeventdescriptor_gettag
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
 - IDvbExtendedEventDescriptor::GetTag
 - dvbsiparser/IDvbExtendedEventDescriptor::GetTag
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
 - IDvbExtendedEventDescriptor.GetTag
---

# IDvbExtendedEventDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a Digital Video Broadcast (DVB) extended event  descriptor.

## -parameters

### -param pbVal [out]

Receives the identifier tag. For DVB  extended event descriptors, this value is "0x4E".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>