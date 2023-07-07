---
UID: NF:dvbsiparser.IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency
title: IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency (dvbsiparser.h)
description: Gets the center frequency from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.
helpviewer_keywords: ["GetRecordFrequency","GetRecordFrequency method [Microsoft TV Technologies]","GetRecordFrequency method [Microsoft TV Technologies]","IIsdbTerrestrialDeliverySystemDescriptor interface","IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies]","GetRecordFrequency method","IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency","IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency","dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency","mstv.iisdbterrestrialdeliverysystemdescriptor_getrecordfrequency"]
old-location: mstv\iisdbterrestrialdeliverysystemdescriptor_getrecordfrequency.htm
tech.root: mstv
ms.assetid: 9040dcc9-49c8-4c3b-ad86-7dc38d1722b9
ms.date: 12/05/2018
ms.keywords: GetRecordFrequency, GetRecordFrequency method [Microsoft TV Technologies], GetRecordFrequency method [Microsoft TV Technologies],IIsdbTerrestrialDeliverySystemDescriptor interface, IIsdbTerrestrialDeliverySystemDescriptor interface [Microsoft TV Technologies],GetRecordFrequency method, IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency, IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency, dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency, mstv.iisdbterrestrialdeliverysystemdescriptor_getrecordfrequency
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
 - IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency
 - dvbsiparser/IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency
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
 - IIsdbTerrestrialDeliverySystemDescriptor.GetRecordFrequency
---

# IIsdbTerrestrialDeliverySystemDescriptor::GetRecordFrequency


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the center frequency from an Integrated Services Digital Broadcasting (ISDB) terrestrial delivery system descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the descriptor to return. To get the number of descriptors, call <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-idvbparentalratingdescriptor-getcountofrecords">IIsdbTerrestrialDeliverySystemDescriptor::GetCountOfRecords</a>

### -param pdwVal [out]

Receives the center frequency, in units of 1/7 MHz.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbterrestrialdeliverysystemdescriptor">IIsdbTerrestrialDeliverySystemDescriptor</a>