---
UID: NF:dvbsiparser.IIsdbDataContentDescriptor.GetLength
title: IIsdbDataContentDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbDataContentDescriptor interface","IIsdbDataContentDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbDataContentDescriptor.GetLength","IIsdbDataContentDescriptor::GetLength","dvbsiparser/IIsdbDataContentDescriptor::GetLength","mstv.iisdbdatacontentdescriptor_getlength"]
old-location: mstv\iisdbdatacontentdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 51546c62-5042-460d-a792-2253bd57df13
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbDataContentDescriptor interface, IIsdbDataContentDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbDataContentDescriptor.GetLength, IIsdbDataContentDescriptor::GetLength, dvbsiparser/IIsdbDataContentDescriptor::GetLength, mstv.iisdbdatacontentdescriptor_getlength
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
 - IIsdbDataContentDescriptor::GetLength
 - dvbsiparser/IIsdbDataContentDescriptor::GetLength
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
 - IIsdbDataContentDescriptor.GetLength
---

# IIsdbDataContentDescriptor::GetLength


## -description

 Gets the body length of an Integrated Services Digital Broadcasting (ISDB) data content descriptor, in bytes.

## -parameters

### -param pbVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbdatacontentdescriptor">IIsdbDataContentDescriptor</a>