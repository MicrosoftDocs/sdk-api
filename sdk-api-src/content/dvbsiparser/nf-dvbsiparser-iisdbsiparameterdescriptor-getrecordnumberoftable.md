---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetRecordNumberOfTable
title: IIsdbSIParameterDescriptor::GetRecordNumberOfTable (dvbsiparser.h)
description: Gets the number of table descriptors in a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetRecordNumberOfTable","GetRecordNumberOfTable method [Microsoft TV Technologies]","GetRecordNumberOfTable method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetRecordNumberOfTable method","IIsdbSIParameterDescriptor.GetRecordNumberOfTable","IIsdbSIParameterDescriptor::GetRecordNumberOfTable","dvbsiparser/IIsdbSIParameterDescriptor::GetRecordNumberOfTable","mstv.iisdbsiparameterdescriptor_getrecordnumberoftable"]
old-location: mstv\iisdbsiparameterdescriptor_getrecordnumberoftable.htm
tech.root: mstv
ms.assetid: 12f7af61-494e-4597-8672-47ea9552be62
ms.date: 12/05/2018
ms.keywords: GetRecordNumberOfTable, GetRecordNumberOfTable method [Microsoft TV Technologies], GetRecordNumberOfTable method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetRecordNumberOfTable method, IIsdbSIParameterDescriptor.GetRecordNumberOfTable, IIsdbSIParameterDescriptor::GetRecordNumberOfTable, dvbsiparser/IIsdbSIParameterDescriptor::GetRecordNumberOfTable, mstv.iisdbsiparameterdescriptor_getrecordnumberoftable
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
 - IIsdbSIParameterDescriptor::GetRecordNumberOfTable
 - dvbsiparser/IIsdbSIParameterDescriptor::GetRecordNumberOfTable
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
 - IIsdbSIParameterDescriptor.GetRecordNumberOfTable
---

# IIsdbSIParameterDescriptor::GetRecordNumberOfTable


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

 Gets the number of table descriptors in a service information (SI) parameter descriptor.

## -parameters

### -param pbVal [out]

Receives the number of table descriptors.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>