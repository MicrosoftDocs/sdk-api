---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetLength
title: IIsdbTSInformationDescriptor::GetLength (dvbsiparser.h)
description: Gets the body length of an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetLength method","IIsdbTSInformationDescriptor.GetLength","IIsdbTSInformationDescriptor::GetLength","dvbsiparser/IIsdbTSInformationDescriptor::GetLength","mstv.iisdbtsinformationdescriptor_getlength"]
old-location: mstv\iisdbtsinformationdescriptor_getlength.htm
tech.root: mstv
ms.assetid: 17c74b77-0754-47de-97f8-db1c15707276
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetLength method, IIsdbTSInformationDescriptor.GetLength, IIsdbTSInformationDescriptor::GetLength, dvbsiparser/IIsdbTSInformationDescriptor::GetLength, mstv.iisdbtsinformationdescriptor_getlength
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IIsdbTSInformationDescriptor::GetLength
 - dvbsiparser/IIsdbTSInformationDescriptor::GetLength
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
 - IIsdbTSInformationDescriptor.GetLength
---

# IIsdbTSInformationDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the body length of an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.

## -parameters

### -param pbVal [out]

Receives the body length of the descriptor, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>