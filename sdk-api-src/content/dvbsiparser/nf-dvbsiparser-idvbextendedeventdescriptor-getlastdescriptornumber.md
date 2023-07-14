---
UID: NF:dvbsiparser.IDvbExtendedEventDescriptor.GetLastDescriptorNumber
title: IDvbExtendedEventDescriptor::GetLastDescriptorNumber (dvbsiparser.h)
description: Gets the number of the last descriptor associated with this descriptor from a Digital Video Broadcast (DVB) extended event descriptor.
helpviewer_keywords: ["GetLastDescriptorNumber","GetLastDescriptorNumber method [Microsoft TV Technologies]","GetLastDescriptorNumber method [Microsoft TV Technologies]","IDvbExtendedEventDescriptor interface","IDvbExtendedEventDescriptor interface [Microsoft TV Technologies]","GetLastDescriptorNumber method","IDvbExtendedEventDescriptor.GetLastDescriptorNumber","IDvbExtendedEventDescriptor::GetLastDescriptorNumber","dvbsiparser/IDvbExtendedEventDescriptor::GetLastDescriptorNumber","mstv.idvbextendedeventdescriptor_getlastdescriptornumber"]
old-location: mstv\idvbextendedeventdescriptor_getlastdescriptornumber.htm
tech.root: mstv
ms.assetid: fccfec3b-0177-4a3d-8c82-0cba3633a613
ms.date: 12/05/2018
ms.keywords: GetLastDescriptorNumber, GetLastDescriptorNumber method [Microsoft TV Technologies], GetLastDescriptorNumber method [Microsoft TV Technologies],IDvbExtendedEventDescriptor interface, IDvbExtendedEventDescriptor interface [Microsoft TV Technologies],GetLastDescriptorNumber method, IDvbExtendedEventDescriptor.GetLastDescriptorNumber, IDvbExtendedEventDescriptor::GetLastDescriptorNumber, dvbsiparser/IDvbExtendedEventDescriptor::GetLastDescriptorNumber, mstv.idvbextendedeventdescriptor_getlastdescriptornumber
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
 - IDvbExtendedEventDescriptor::GetLastDescriptorNumber
 - dvbsiparser/IDvbExtendedEventDescriptor::GetLastDescriptorNumber
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
 - IDvbExtendedEventDescriptor.GetLastDescriptorNumber
---

# IDvbExtendedEventDescriptor::GetLastDescriptorNumber


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the number of the last descriptor associated with this descriptor from a Digital Video Broadcast (DVB) extended event descriptor.

## -parameters

### -param pbVal [out]

Receives the last descriptor number.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvbextendedeventdescriptor">IDvbExtendedEventDescriptor</a>