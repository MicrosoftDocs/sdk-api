---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetLength
title: IDvbLogicalChannelDescriptor::GetLength (dvbsiparser.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later. .
helpviewer_keywords: ["GetLength","GetLength method [DirectShow]","GetLength method [DirectShow]","IDvbLogicalChannelDescriptor interface","IDvbLogicalChannelDescriptor interface [DirectShow]","GetLength method","IDvbLogicalChannelDescriptor.GetLength","IDvbLogicalChannelDescriptor::GetLength","IDvbLogicalChannelDescriptorGetLength","dvbsiparser/IDvbLogicalChannelDescriptor::GetLength","mstv.idvblogicalchanneldescriptor_getlength"]
old-location: mstv\idvblogicalchanneldescriptor_getlength.htm
tech.root: mstv
ms.assetid: 20c0f2a8-e4f5-4516-8c19-30cd19f0816e
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [DirectShow], GetLength method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetLength method, IDvbLogicalChannelDescriptor.GetLength, IDvbLogicalChannelDescriptor::GetLength, IDvbLogicalChannelDescriptorGetLength, dvbsiparser/IDvbLogicalChannelDescriptor::GetLength, mstv.idvblogicalchanneldescriptor_getlength
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
 - IDvbLogicalChannelDescriptor::GetLength
 - dvbsiparser/IDvbLogicalChannelDescriptor::GetLength
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
 - IDvbLogicalChannelDescriptor.GetLength
---

# IDvbLogicalChannelDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.</div>
<div> </div>




The <b>GetLength</b> method returns the length of the descriptor body.

## -parameters

### -param pbVal [out]

Receives the length of the descriptor body, in bytes.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a>