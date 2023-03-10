---
UID: NF:dvbsiparser.IDvbContentDescriptor.GetLength
title: IDvbContentDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) content descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbContentDescriptor interface","IDvbContentDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbContentDescriptor.GetLength","IDvbContentDescriptor::GetLength","dvbsiparser/IDvbContentDescriptor::GetLength","mstv.idvbcontentdescriptor_getlength"]
old-location: mstv\idvbcontentdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 3e937c51-e143-4b13-a16a-279bd3690feb
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbContentDescriptor interface, IDvbContentDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbContentDescriptor.GetLength, IDvbContentDescriptor::GetLength, dvbsiparser/IDvbContentDescriptor::GetLength, mstv.idvbcontentdescriptor_getlength
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
 - IDvbContentDescriptor::GetLength
 - dvbsiparser/IDvbContentDescriptor::GetLength
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
 - IDvbContentDescriptor.GetLength
---

# IDvbContentDescriptor::GetLength


## -description

Gets the body length of a Digital Video Broadcast (DVB) content descriptor.

## -parameters

### -param pbVal [out]

Receives the content descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbcontentdescriptor">IDvbContentDescriptor</a>