---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetCASystemId
title: IIsdbCADescriptor::GetCASystemId (dvbsiparser.h)
description: Gets the conditional access (CA) system identifier from a conditional access descriptor.
helpviewer_keywords: ["GetCASystemId","GetCASystemId method [Microsoft TV Technologies]","GetCASystemId method [Microsoft TV Technologies]","IIsdbCADescriptor interface","IIsdbCADescriptor interface [Microsoft TV Technologies]","GetCASystemId method","IIsdbCADescriptor.GetCASystemId","IIsdbCADescriptor::GetCASystemId","dvbsiparser/IIsdbCADescriptor::GetCASystemId","mstv.iisdbcadescriptor_getcasystemid"]
old-location: mstv\iisdbcadescriptor_getcasystemid.htm
tech.root: mstv
ms.assetid: 834825d4-f92d-4cca-bf15-a3f94647c4f1
ms.date: 12/05/2018
ms.keywords: GetCASystemId, GetCASystemId method [Microsoft TV Technologies], GetCASystemId method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetCASystemId method, IIsdbCADescriptor.GetCASystemId, IIsdbCADescriptor::GetCASystemId, dvbsiparser/IIsdbCADescriptor::GetCASystemId, mstv.iisdbcadescriptor_getcasystemid
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
 - IIsdbCADescriptor::GetCASystemId
 - dvbsiparser/IIsdbCADescriptor::GetCASystemId
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
 - IIsdbCADescriptor.GetCASystemId
---

# IIsdbCADescriptor::GetCASystemId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the conditional access (CA) system identifier from  a conditional access descriptor.

## -parameters

### -param pwVal [out]

Receives the conditional access system identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcadescriptor">IIsdbCADescriptor</a>