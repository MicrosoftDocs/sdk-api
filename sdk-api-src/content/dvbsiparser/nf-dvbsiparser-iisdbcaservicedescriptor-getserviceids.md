---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetServiceIds
title: IIsdbCAServiceDescriptor::GetServiceIds (dvbsiparser.h)
description: Gets the service identifier (ID) records from a conditional access (CA) service descriptor.
helpviewer_keywords: ["GetServiceIds","GetServiceIds method [Microsoft TV Technologies]","GetServiceIds method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetServiceIds method","IIsdbCAServiceDescriptor.GetServiceIds","IIsdbCAServiceDescriptor::GetServiceIds","dvbsiparser/IIsdbCAServiceDescriptor::GetServiceIds","mstv.iisdbcaservicedescriptor_getserviceids"]
old-location: mstv\iisdbcaservicedescriptor_getserviceids.htm
tech.root: mstv
ms.assetid: f2a6d1f2-2cd5-4f8c-97e1-33880ffb0449
ms.date: 12/05/2018
ms.keywords: GetServiceIds, GetServiceIds method [Microsoft TV Technologies], GetServiceIds method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetServiceIds method, IIsdbCAServiceDescriptor.GetServiceIds, IIsdbCAServiceDescriptor::GetServiceIds, dvbsiparser/IIsdbCAServiceDescriptor::GetServiceIds, mstv.iisdbcaservicedescriptor_getserviceids
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
 - IIsdbCAServiceDescriptor::GetServiceIds
 - dvbsiparser/IIsdbCAServiceDescriptor::GetServiceIds
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
 - IIsdbCAServiceDescriptor.GetServiceIds
---

# IIsdbCAServiceDescriptor::GetServiceIds


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the service identifier (ID) records from a conditional access (CA) service descriptor.

## -parameters

### -param pbNumServiceIds [in, out]

On input specifies the expected number of service ID records. On output returns the actual number of records.

### -param pwServiceIds [out]

Receives the service ID records.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>