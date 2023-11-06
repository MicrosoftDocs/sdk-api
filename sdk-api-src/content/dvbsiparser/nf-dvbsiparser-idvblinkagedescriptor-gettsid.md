---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetTSId
title: IDvbLinkageDescriptor::GetTSId (dvbsiparser.h)
description: Gets the identifier of the transport stream containing the information service from a DVB linkage descriptor.
helpviewer_keywords: ["GetTSId","GetTSId method [Microsoft TV Technologies]","GetTSId method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetTSId method","IDvbLinkageDescriptor.GetTSId","IDvbLinkageDescriptor::GetTSId","dvbsiparser/IDvbLinkageDescriptor::GetTSId","mstv.idvblinkagedescriptor_gettsid"]
old-location: mstv\idvblinkagedescriptor_gettsid.htm
tech.root: mstv
ms.assetid: 263f3ff1-33a6-4c40-bcdf-049c4dbaf2ef
ms.date: 12/05/2018
ms.keywords: GetTSId, GetTSId method [Microsoft TV Technologies], GetTSId method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetTSId method, IDvbLinkageDescriptor.GetTSId, IDvbLinkageDescriptor::GetTSId, dvbsiparser/IDvbLinkageDescriptor::GetTSId, mstv.idvblinkagedescriptor_gettsid
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: None supported
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Dvbsiparser.idl
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
 - IDvbLinkageDescriptor::GetTSId
 - dvbsiparser/IDvbLinkageDescriptor::GetTSId
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
 - IDvbLinkageDescriptor.GetTSId
---

# IDvbLinkageDescriptor::GetTSId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the identifier of the  transport stream containing the information service from a DVB linkage descriptor.

## -parameters

### -param pwVal [out]

Receives the transport stream identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>