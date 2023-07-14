---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetTag
title: IIsdbTerrestrialDeliverySystemDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Digital Services Broadcasting (ISDB) terrestrial delivery system descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbTerrestrialDeliverySystemDescriptor interface","IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbTerrestrialDeliverySystemDescriptor.GetTag","IIsdbTerrestrialDeliverySystemDescriptor::GetTag","dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetTag","mstv.iisdbterrestrialdeliverysystemdescriptor_gettag"]
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 15b70e2e-21e0-406c-9d7a-32031114d50b
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbTerrestrialDeliverySystemDescriptor.GetTag, IIsdbTerrestrialDeliverySystemDescriptor::GetTag, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetTag, mstv.iisdbterrestrialdeliverysystemdescriptor_gettag
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
 - IIsdbTerrestrialDeliverySystemDescriptor::GetTag
 - dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetTag
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
 - IIsdbTerrestrialDeliverySystemDescriptor.GetTag
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an Integrated Digital Services Broadcasting (ISDB) terrestrial delivery system descriptor.

## -parameters

### -param pbVal [out]

Receives the terrestrial delivery system descriptor tag. For terrestrial delivery system descriptors, this value is 0xFA.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor">IIsdbTerrestrialDeliverySystemDescriptor</a>