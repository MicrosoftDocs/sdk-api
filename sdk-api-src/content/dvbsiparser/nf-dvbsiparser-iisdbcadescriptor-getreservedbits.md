---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetReservedBits
title: IIsdbCADescriptor::GetReservedBits (dvbsiparser.h)
description: Gets the reserved bits from a conditional access (CA) descriptor.
helpviewer_keywords: ["GetReservedBits","GetReservedBits method [Microsoft TV Technologies]","GetReservedBits method [Microsoft TV Technologies]","IIsdbCADescriptor interface","IIsdbCADescriptor interface [Microsoft TV Technologies]","GetReservedBits method","IIsdbCADescriptor.GetReservedBits","IIsdbCADescriptor::GetReservedBits","dvbsiparser/IIsdbCADescriptor::GetReservedBits","mstv.iisdbcadescriptor_getreservedbits"]
old-location: mstv\iisdbcadescriptor_getreservedbits.htm
tech.root: mstv
ms.assetid: c45295f9-df77-4a23-b6c2-65d5b2c9c360
ms.date: 12/05/2018
ms.keywords: GetReservedBits, GetReservedBits method [Microsoft TV Technologies], GetReservedBits method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetReservedBits method, IIsdbCADescriptor.GetReservedBits, IIsdbCADescriptor::GetReservedBits, dvbsiparser/IIsdbCADescriptor::GetReservedBits, mstv.iisdbcadescriptor_getreservedbits
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
 - IIsdbCADescriptor::GetReservedBits
 - dvbsiparser/IIsdbCADescriptor::GetReservedBits
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
 - IIsdbCADescriptor.GetReservedBits
---

# IIsdbCADescriptor::GetReservedBits


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the reserved bits from a conditional access (CA) descriptor.

## -parameters

### -param pbVal [out]

Receives the reserved bits.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcadescriptor">IIsdbCADescriptor</a>