---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableDescriptionBytes
title: IIsdbSIParameterDescriptor::GetTableDescriptionBytes (dvbsiparser.h)
description: Gets description data from a table descriptor in a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetTableDescriptionBytes","GetTableDescriptionBytes method [Microsoft TV Technologies]","GetTableDescriptionBytes method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetTableDescriptionBytes method","IIsdbSIParameterDescriptor.GetTableDescriptionBytes","IIsdbSIParameterDescriptor::GetTableDescriptionBytes","dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionBytes","mstv.iisdbsiparameterdescriptor_gettabledescriptionbytes"]
old-location: mstv\iisdbsiparameterdescriptor_gettabledescriptionbytes.htm
tech.root: mstv
ms.assetid: dd73b221-b7b5-43c8-bbdf-f1ea559a0a4e
ms.date: 12/05/2018
ms.keywords: GetTableDescriptionBytes, GetTableDescriptionBytes method [Microsoft TV Technologies], GetTableDescriptionBytes method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableDescriptionBytes method, IIsdbSIParameterDescriptor.GetTableDescriptionBytes, IIsdbSIParameterDescriptor::GetTableDescriptionBytes, dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionBytes, mstv.iisdbsiparameterdescriptor_gettabledescriptionbytes
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
 - IIsdbSIParameterDescriptor::GetTableDescriptionBytes
 - dvbsiparser/IIsdbSIParameterDescriptor::GetTableDescriptionBytes
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
 - IIsdbSIParameterDescriptor.GetTableDescriptionBytes
---

# IIsdbSIParameterDescriptor::GetTableDescriptionBytes


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets description data from a table descriptor in a service information (SI) parameter descriptor.

## -parameters

### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.

### -param pbBufferLength [in, out]

On input specifies the length of the table descriptor data that is retrieved, in bytes. On output returns the actual data length.

### -param pbBuffer [out]

Receives the table descriptor data.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>



<a href="/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>