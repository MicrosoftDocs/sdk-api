---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetLength
title: IDvbExtendedEventDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetLength method","IDvbExtendedEventDescriptor.GetLength","IDvbExtendedEventDescriptor::GetLength","dvbsiparser/IDvbExtendedEventDescriptor::GetLength","mstv.idvbextendedeventdescriptor_getlength"]
old-location: mstv\idvbextendedeventdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 5109cdff-27a0-41e5-9b9e-25a82d176e14
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetLength method, IDvbExtendedEventDescriptor.GetLength, IDvbExtendedEventDescriptor::GetLength, dvbsiparser/IDvbExtendedEventDescriptor::GetLength, mstv.idvbextendedeventdescriptor_getlength
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
 - IDvbExtendedEventDescriptor::GetLength
 - dvbsiparser/IDvbExtendedEventDescriptor::GetLength
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
 - IDvbExtendedEventDescriptor.GetLength
---

# IDvbExtendedEventDescriptor::GetLength


## -description

Gets the body length of a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param pbVal [out]

Receives the event descriptor length.

## -returns

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>