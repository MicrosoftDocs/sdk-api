---
UID: NF:dvbsiparser.IIsdbCADescriptor.GetLength
title: IIsdbCADescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of a conditional access (CA) descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbCADescriptor interface","IIsdbCADescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbCADescriptor.GetLength","IIsdbCADescriptor::GetLength","dvbsiparser/IIsdbCADescriptor::GetLength","mstv.iisdbcadescriptor_getlength"]
old-location: mstv\iisdbcadescriptor_getlength.htm
tech.root: mstv
ms.assetid: 25331811-51d4-4009-8fc2-825a8de33dcf
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbCADescriptor interface, IIsdbCADescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbCADescriptor.GetLength, IIsdbCADescriptor::GetLength, dvbsiparser/IIsdbCADescriptor::GetLength, mstv.iisdbcadescriptor_getlength
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
 - IIsdbCADescriptor::GetLength
 - dvbsiparser/IIsdbCADescriptor::GetLength
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
 - IIsdbCADescriptor.GetLength
---

# IIsdbCADescriptor::GetLength


## -description

 Gets the body length of a conditional access (CA) descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcadescriptor">IIsdbCADescriptor</a>