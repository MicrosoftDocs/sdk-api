---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetCAPID
title: IIsdbCADescriptor::GetCAPID (dvbsiparser.h)
description: Gets the conditional access (CA) program identifier (PID) from a conditional access descriptor.
helpviewer_keywords: ["GetCAPID","GetCAPID method [Microsoft TV Technologies]","GetCAPID method [Microsoft TV Technologies]","IIsdbCADescriptor interface","IIsdbCADescriptor interface [Microsoft TV Technologies]","GetCAPID method","IIsdbCADescriptor.GetCAPID","IIsdbCADescriptor::GetCAPID","dvbsiparser/IIsdbCADescriptor::GetCAPID","mstv.iisdbcadescriptor_getcapid"]
old-location: mstv\iisdbcadescriptor_getcapid.htm
tech.root: mstv
ms.assetid: 9d4815f2-7f58-4952-a64b-067c99ae8d43
ms.date: 12/05/2018
ms.keywords: GetCAPID, GetCAPID method [Microsoft TV Technologies], GetCAPID method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetCAPID method, IIsdbCADescriptor.GetCAPID, IIsdbCADescriptor::GetCAPID, dvbsiparser/IIsdbCADescriptor::GetCAPID, mstv.iisdbcadescriptor_getcapid
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
 - IIsdbCADescriptor::GetCAPID
 - dvbsiparser/IIsdbCADescriptor::GetCAPID
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
 - IIsdbCADescriptor.GetCAPID
---

# IIsdbCADescriptor::GetCAPID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the conditional access (CA) program identifier (PID) from a conditional access descriptor.

## -parameters

### -param pwVal [out]

Receives the conditional access PID value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcadescriptor">IIsdbCADescriptor</a>