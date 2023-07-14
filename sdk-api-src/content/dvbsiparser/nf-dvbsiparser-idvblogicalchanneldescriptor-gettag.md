---
UID: NF:dvbsiparser.IDvbLogicalChannelDescriptor.GetTag
title: IDvbLogicalChannelDescriptor::GetTag (dvbsiparser.h)
description: Note  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.  .
helpviewer_keywords: ["GetTag","GetTag method [DirectShow]","GetTag method [DirectShow]","IDvbLogicalChannelDescriptor interface","IDvbLogicalChannelDescriptor interface [DirectShow]","GetTag method","IDvbLogicalChannelDescriptor.GetTag","IDvbLogicalChannelDescriptor::GetTag","IDvbLogicalChannelDescriptorGetTag","dvbsiparser/IDvbLogicalChannelDescriptor::GetTag","mstv.idvblogicalchanneldescriptor_gettag"]
old-location: mstv\idvblogicalchanneldescriptor_gettag.htm
tech.root: mstv
ms.assetid: fce4b74e-e7bb-419d-bd5a-849c2d050ee9
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [DirectShow], GetTag method [DirectShow],IDvbLogicalChannelDescriptor interface, IDvbLogicalChannelDescriptor interface [DirectShow],GetTag method, IDvbLogicalChannelDescriptor.GetTag, IDvbLogicalChannelDescriptor::GetTag, IDvbLogicalChannelDescriptorGetTag, dvbsiparser/IDvbLogicalChannelDescriptor::GetTag, mstv.idvblogicalchanneldescriptor_gettag
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
 - IDvbLogicalChannelDescriptor::GetTag
 - dvbsiparser/IDvbLogicalChannelDescriptor::GetTag
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
 - IDvbLogicalChannelDescriptor.GetTag
---

# IDvbLogicalChannelDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

<div class="alert"><b>Note</b>  This topic applies to Update Rollup 2 for Microsoft Windows XP Media Center Edition 2005 and later.
        </div>
<div> </div>




The <b>GetTag</b> method returns the descriptor tag.

## -parameters

### -param pbVal [out]

Receives the descriptor tag.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblogicalchanneldescriptor">IDvbLogicalChannelDescriptor</a>