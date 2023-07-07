---
UID: NF:dvbsiparser.IIsdbLogoTransmissionDescriptor.GetLogoId
title: IIsdbLogoTransmissionDescriptor::GetLogoId (dvbsiparser.h)
description: Gets the logo identifier from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.
helpviewer_keywords: ["GetLogoId","GetLogoId method [Microsoft TV Technologies]","GetLogoId method [Microsoft TV Technologies]","IIsdbLogoTransmissionDescriptor interface","IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies]","GetLogoId method","IIsdbLogoTransmissionDescriptor.GetLogoId","IIsdbLogoTransmissionDescriptor::GetLogoId","dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoId","mstv.iisdblogotransmissiondescriptor_getlogoid"]
old-location: mstv\iisdblogotransmissiondescriptor_getlogoid.htm
tech.root: mstv
ms.assetid: f4c11012-5d37-4d8f-944b-edfa50719b12
ms.date: 12/05/2018
ms.keywords: GetLogoId, GetLogoId method [Microsoft TV Technologies], GetLogoId method [Microsoft TV Technologies],IIsdbLogoTransmissionDescriptor interface, IIsdbLogoTransmissionDescriptor interface [Microsoft TV Technologies],GetLogoId method, IIsdbLogoTransmissionDescriptor.GetLogoId, IIsdbLogoTransmissionDescriptor::GetLogoId, dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoId, mstv.iisdblogotransmissiondescriptor_getlogoid
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
 - IIsdbLogoTransmissionDescriptor::GetLogoId
 - dvbsiparser/IIsdbLogoTransmissionDescriptor::GetLogoId
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
 - IIsdbLogoTransmissionDescriptor.GetLogoId
---

# IIsdbLogoTransmissionDescriptor::GetLogoId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the logo identifier from an Integrated Services Digital Broadcasting (ISDB) logo transmission descriptor.

## -parameters

### -param pwVal [out]

Receives the logo identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdblogotransmissiondescriptor">IIsdbLogoTransmissionDescriptor</a>