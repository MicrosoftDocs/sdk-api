---
UID: NF:dvbsiparser.IIsdbTSInformationDescriptor.GetTag
title: IIsdbTSInformationDescriptor::GetTag (dvbsiparser.h)
description: Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbTSInformationDescriptor interface","IIsdbTSInformationDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbTSInformationDescriptor.GetTag","IIsdbTSInformationDescriptor::GetTag","dvbsiparser/IIsdbTSInformationDescriptor::GetTag","mstv.iisdbtsinformationdescriptor_gettag"]
old-location: mstv\iisdbtsinformationdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 77a7b225-2e7e-4fa2-a8f0-a5f18850cde6
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbTSInformationDescriptor interface, IIsdbTSInformationDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbTSInformationDescriptor.GetTag, IIsdbTSInformationDescriptor::GetTag, dvbsiparser/IIsdbTSInformationDescriptor::GetTag, mstv.iisdbtsinformationdescriptor_gettag
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
 - IIsdbTSInformationDescriptor::GetTag
 - dvbsiparser/IIsdbTSInformationDescriptor::GetTag
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
 - IIsdbTSInformationDescriptor.GetTag
---

# IIsdbTSInformationDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Receives the tag that identifies an Integrated Services Digital Broadcasting (ISDB) transport stream (TS) information descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For ISDB TS information descriptors, this value is 0xCD.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbtsinformationdescriptor">IIsdbTSInformationDescriptor</a>