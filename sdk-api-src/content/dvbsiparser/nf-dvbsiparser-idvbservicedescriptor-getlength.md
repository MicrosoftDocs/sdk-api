---
UID: NF:dvbsiparser.IDvbServiceDescriptor.GetLength
title: IDvbServiceDescriptor::GetLength (dvbsiparser.h)
description: Gets the length of a Digital Video Broadcast (DVB) service descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbServiceDescriptor interface","IDvbServiceDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbServiceDescriptor.GetLength","IDvbServiceDescriptor::GetLength","dvbsiparser/IDvbServiceDescriptor::GetLength","mstv.idvbservicedescriptor_getlength"]
old-location: mstv\idvbservicedescriptor_getlength.htm
tech.root: mstv
ms.assetid: e8c35777-0a54-4b26-b5a2-629ba3cb3928
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbServiceDescriptor interface, IDvbServiceDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbServiceDescriptor.GetLength, IDvbServiceDescriptor::GetLength, dvbsiparser/IDvbServiceDescriptor::GetLength, mstv.idvbservicedescriptor_getlength
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
 - IDvbServiceDescriptor::GetLength
 - dvbsiparser/IDvbServiceDescriptor::GetLength
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
 - IDvbServiceDescriptor.GetLength
---

# IDvbServiceDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the length of a Digital Video Broadcast (DVB) service descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor length, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbservicedescriptor">IDvbServiceDescriptor</a>