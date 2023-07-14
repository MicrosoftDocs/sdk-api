---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetCountOfRecords
title: IDvbLogicalChannelDescriptor::GetCountOfRecords (dvbsiparser.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. .
helpviewer_keywords: ["GetCountOfRecords","GetCountOfRecords method [DirectShow]","GetCountOfRecords method [DirectShow]","IDvbLogicalChannelDescriptor interface","IDvbLogicalChannelDescriptor interface [DirectShow]","GetCountOfRecords method","IDvbLogicalChannelDescriptor.GetCountOfRecords","IDvbLogicalChannelDescriptor::GetCountOfRecords","IDvbLogicalChannelDescriptorGetCountOfRecords","dvbsiparser/IDvbLogicalChannelDescriptor::GetCountOfRecords","mstv.idvblogicalchanneldescriptor_getcountofrecords"]
old-location: mstv\idvblogicalchanneldescriptor_getcountofrecords.htm
tech.root: mstv
ms.assetid: 97cadf6c-2549-4a7f-9ecb-c16298769a21
ms.date: 12/05/2018
ms.keywords: GetCountOfRecords, GetCountOfRecords method [DirectShow], GetCountOfRecords method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetCountOfRecords method, IDvbLogicalChannelDescriptor.GetCountOfRecords, IDvbLogicalChannelDescriptor::GetCountOfRecords, IDvbLogicalChannelDescriptorGetCountOfRecords, dvbsiparser/IDvbLogicalChannelDescriptor::GetCountOfRecords, mstv.idvblogicalchanneldescriptor_getcountofrecords
req.header: dvbsiparser.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
 - IDvbLogicalChannelDescriptor::GetCountOfRecords
 - dvbsiparser/IDvbLogicalChannelDescriptor::GetCountOfRecords
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
 - IDvbLogicalChannelDescriptor.GetCountOfRecords
---

# IDvbLogicalChannelDescriptor::GetCountOfRecords


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>




The <b>GetCountOfRecords</b> method returns the number of records in the logical channel descriptor.

## -parameters

### -param pbVal [out]

Receives the number of records in the descriptor.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a>