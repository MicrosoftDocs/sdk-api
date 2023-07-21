---
UID: NF:dvbsiparser.IDvbDefaultAuthorityDescriptor.GetTag
title: IDvbDefaultAuthorityDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbDefaultAuthorityDescriptor interface","IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbDefaultAuthorityDescriptor.GetTag","IDvbDefaultAuthorityDescriptor::GetTag","dvbsiparser/IDvbDefaultAuthorityDescriptor::GetTag","mstv.idvbdefaultauthoritydescriptor_gettag"]
old-location: mstv\idvbdefaultauthoritydescriptor_gettag.htm
tech.root: mstv
ms.assetid: d98d1a45-1d72-4142-8bb4-15ac4f738813
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbDefaultAuthorityDescriptor interface, IDvbDefaultAuthorityDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbDefaultAuthorityDescriptor.GetTag, IDvbDefaultAuthorityDescriptor::GetTag, dvbsiparser/IDvbDefaultAuthorityDescriptor::GetTag, mstv.idvbdefaultauthoritydescriptor_gettag
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
 - IDvbDefaultAuthorityDescriptor::GetTag
 - dvbsiparser/IDvbDefaultAuthorityDescriptor::GetTag
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
 - IDvbDefaultAuthorityDescriptor.GetTag
---

# IDvbDefaultAuthorityDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag from the default authority descriptor for a Digital Video Broadcast (DVB) content reference identifier (CRID).

## -parameters

### -param pbVal [out]

Receives the content descriptor tag. For default authority descriptors, this tag value is "0x73".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbdefaultauthoritydescriptor">IDvbDefaultAuthorityDescriptor</a>