---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetTag
title: IIsdbLogoTransmissionDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbLogoTransmissionDescriptor interface","IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbLogoTransmissionDescriptor.GetTag","IIsdbLogoTransmissionDescriptor::GetTag","dvbsiparser/IIsdbLogoTransmissionDescriptor::GetTag","mstv.iisdblogotransmissiondescriptor_gettag"]
old-location: mstv\iisdblogotransmissiondescriptor_gettag.htm
tech.root: mstv
ms.assetid: 7ad7d7b5-a20f-4d03-b699-a39fe7ea7568
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbLogoTransmissionDescriptor.GetTag, IIsdbLogoTransmissionDescriptor::GetTag, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetTag, mstv.iisdblogotransmissiondescriptor_gettag
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
 - IIsdbLogoTransmissionDescriptor::GetTag
 - dvbsiparser/IIsdbLogoTransmissionDescriptor::GetTag
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
 - IIsdbLogoTransmissionDescriptor.GetTag
---

# IIsdbLogoTransmissionDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For ISDB logo transmission descriptors, this value is 0xCF.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdblogotransmissiondescriptor">IIsdbLogoTransmissionDescriptor</a>