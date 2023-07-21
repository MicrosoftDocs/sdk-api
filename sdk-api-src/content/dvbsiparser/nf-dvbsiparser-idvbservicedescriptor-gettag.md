---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetTag
title: IDvbServiceDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag identifying a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbServiceDescriptor.GetTag","IDvbServiceDescriptor::GetTag","dvbsiparser/IDvbServiceDescriptor::GetTag","mstv.idvbservicedescriptor_gettag"]
old-location: mstv\idvbservicedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 0cdf6279-3156-43eb-97e3-58a4f9d93cc6
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbServiceDescriptor.GetTag, IDvbServiceDescriptor::GetTag, dvbsiparser/IDvbServiceDescriptor::GetTag, mstv.idvbservicedescriptor_gettag
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
 - IDvbServiceDescriptor::GetTag
 - dvbsiparser/IDvbServiceDescriptor::GetTag
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
 - IDvbServiceDescriptor.GetTag
---

# IDvbServiceDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag identifying a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param pbVal [out]

Receives the service descriptor tag. This value is 0x48 for service descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>