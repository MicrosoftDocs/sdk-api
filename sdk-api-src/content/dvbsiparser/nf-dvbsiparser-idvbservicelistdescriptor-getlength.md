---
UID: NF:dvbsiparser.IDvbServiceListDescriptor.GetLength
title: IDvbServiceListDescriptor::GetLength (dvbsiparser.h)
description: Gets the descriptor_length field value from a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbServiceListDescriptor interface","IDvbServiceListDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbServiceListDescriptor.GetLength","IDvbServiceListDescriptor::GetLength","dvbsiparser/IDvbServiceListDescriptor::GetLength","mstv.idvbservicelistdescriptor_getlength"]
old-location: mstv\idvbservicelistdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 06c161ce-b830-4375-8ed6-19403857f433
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbServiceListDescriptor interface, IDvbServiceListDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbServiceListDescriptor.GetLength, IDvbServiceListDescriptor::GetLength, dvbsiparser/IDvbServiceListDescriptor::GetLength, mstv.idvbservicelistdescriptor_getlength
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
 - IDvbServiceListDescriptor::GetLength
 - dvbsiparser/IDvbServiceListDescriptor::GetLength
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
 - IDvbServiceListDescriptor.GetLength
---

# IDvbServiceListDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the descriptor_length field value from a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicelistdescriptor">IDvbServiceListDescriptor</a>