---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetCASystemId
title: IIsdbCAServiceDescriptor::GetCASystemId (dvbsiparser.h)
description: Gets the conditional access (CA) system identifier from a CA service descriptor.
helpviewer_keywords: ["GetCASystemId","GetCASystemId method [Microsoft TV Technologies]","GetCASystemId method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetCASystemId method","IIsdbCAServiceDescriptor.GetCASystemId","IIsdbCAServiceDescriptor::GetCASystemId","dvbsiparser/IIsdbCAServiceDescriptor::GetCASystemId","mstv.iisdbcaservicedescriptor_getcasystemid"]
old-location: mstv\iisdbcaservicedescriptor_getcasystemid.htm
tech.root: mstv
ms.assetid: 48148c5c-30e1-4028-8baf-692141d79fad
ms.date: 12/05/2018
ms.keywords: GetCASystemId, GetCASystemId method [Microsoft TV Technologies], GetCASystemId method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetCASystemId method, IIsdbCAServiceDescriptor.GetCASystemId, IIsdbCAServiceDescriptor::GetCASystemId, dvbsiparser/IIsdbCAServiceDescriptor::GetCASystemId, mstv.iisdbcaservicedescriptor_getcasystemid
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
 - IIsdbCAServiceDescriptor::GetCASystemId
 - dvbsiparser/IIsdbCAServiceDescriptor::GetCASystemId
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
 - IIsdbCAServiceDescriptor.GetCASystemId
---

# IIsdbCAServiceDescriptor::GetCASystemId


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the conditional access (CA) system identifier from a CA service descriptor.

## -parameters

### -param pwVal [out]

Receives the conditional access system identifier.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>