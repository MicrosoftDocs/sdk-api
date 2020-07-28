---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTableId
title: IIsdbSIParameterDescriptor::GetTableId (dvbsiparser.h)
description: Gets an identifier for a table descriptor in a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetTableId","GetTableId method [Microsoft TV Technologies]","GetTableId method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetTableId method","IIsdbSIParameterDescriptor.GetTableId","IIsdbSIParameterDescriptor::GetTableId","dvbsiparser/IIsdbSIParameterDescriptor::GetTableId","mstv.iisdbsiparameterdescriptor_gettableid"]
old-location: mstv\iisdbsiparameterdescriptor_gettableid.htm
tech.root: mstv
ms.assetid: 43b19e3d-20b0-4356-9c84-f47006635e2c
ms.date: 12/05/2018
ms.keywords: GetTableId, GetTableId method [Microsoft TV Technologies], GetTableId method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTableId method, IIsdbSIParameterDescriptor.GetTableId, IIsdbSIParameterDescriptor::GetTableId, dvbsiparser/IIsdbSIParameterDescriptor::GetTableId, mstv.iisdbsiparameterdescriptor_gettableid
f1_keywords:
- dvbsiparser/IIsdbSIParameterDescriptor.GetTableId
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- dvbsiparser.h
api_name:
- IIsdbSIParameterDescriptor.GetTableId
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IIsdbSIParameterDescriptor::GetTableId


## -description


Gets an identifier for a table descriptor in a service information (SI) parameter descriptor. 


## -parameters




### -param bRecordIndex [in]

Zero-based index of the SI table descriptor. To get the number of table descriptors, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a> method.


### -param pbVal [out]

Receives the table descriptor identifier.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dvbsiparser/nf-dvbsiparser-iisdbsiparameterdescriptor-getrecordnumberoftable">IIsdbSIParameterDescriptor::GetRecordNumberOfTable</a>
 

 

