---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableDescriptionLength
title: IIsdbSIParameterDescriptor::GetTableDescriptionLength (dvbsiparser.h)
description: Gets the body length of a table descriptor in a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetTableDescriptionLength","GetTableDescriptionLength method [Microsoft TV Technologies]","GetTableDescriptionLength method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetTableDescriptionLength method","IIsdbSIParameterDescriptor.GetTableDescriptionLength","IIsdbSIParameterDescriptor::GetTableDescriptionLength","dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionLength","mstv.iisdbsiparameterdescriptor_gettabledescriptionlength"]
old-location: mstv\iisdbsiparameterdescriptor_gettabledescriptionlength.htm
tech.root: mstv
ms.assetid: 3dc78381-ac39-4e88-bfe2-bfb91c993576
ms.date: 12/05/2018
ms.keywords: GetTableDescriptionLength, GetTableDescriptionLength method [Microsoft TV Technologies], GetTableDescriptionLength method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableDescriptionLength method, IIsdbSIParameterDescriptor.GetTableDescriptionLength, IIsdbSIParameterDescriptor::GetTableDescriptionLength, dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionLength, mstv.iisdbsiparameterdescriptor_gettabledescriptionlength
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
 - IIsdbSIParameterDescriptor::GetTableDescriptionLength
 - dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionLength
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
 - IIsdbSIParameterDescriptor.GetTableDescriptionLength
---

# IIsdbSIParameterDescriptor::GetTableDescriptionLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of a table descriptor in a service information (SI) parameter descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.

### -param pbVal [out]

Receives the length of the table descriptor, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>