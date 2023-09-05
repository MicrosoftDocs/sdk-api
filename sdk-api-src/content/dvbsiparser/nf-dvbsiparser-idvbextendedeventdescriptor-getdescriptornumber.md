---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetDescriptorNumber
title: IDvbExtendedEventDescriptor::GetDescriptorNumber (dvbsiparser.h)
description: Gets the descriptor number from a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetDescriptorNumber","GetDescriptorNumber method [Microsoft TV Technologies]","GetDescriptorNumber method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetDescriptorNumber method","IDvbExtendedEventDescriptor.GetDescriptorNumber","IDvbExtendedEventDescriptor::GetDescriptorNumber","dvbsiparser/IDvbExtendedEventDescriptor::GetDescriptorNumber","mstv.idvbextendedeventdescriptor_getdescriptornumber"]
old-location: mstv\idvbextendedeventdescriptor_getdescriptornumber.htm
tech.root: mstv
ms.assetid: 5cf156fe-bfdd-444d-be4e-422c11ab08dc
ms.date: 12/05/2018
ms.keywords: GetDescriptorNumber, GetDescriptorNumber method [Microsoft TV Technologies], GetDescriptorNumber method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetDescriptorNumber method, IDvbExtendedEventDescriptor.GetDescriptorNumber, IDvbExtendedEventDescriptor::GetDescriptorNumber, dvbsiparser/IDvbExtendedEventDescriptor::GetDescriptorNumber, mstv.idvbextendedeventdescriptor_getdescriptornumber
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
 - IDvbExtendedEventDescriptor::GetDescriptorNumber
 - dvbsiparser/IDvbExtendedEventDescriptor::GetDescriptorNumber
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
 - IDvbExtendedEventDescriptor.GetDescriptorNumber
---

# IDvbExtendedEventDescriptor::GetDescriptorNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the descriptor number from a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param pbVal [out]

Receives the descriptor number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>