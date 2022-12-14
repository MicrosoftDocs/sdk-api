---
UID: NF:dvbsiparser.IDvbLinkageDescriptor.GetTag
title: IDvbLinkageDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a Digital Video Broadcast (DVB) linkage descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IDvbLinkageDescriptor interface","IDvbLinkageDescriptor interface [Microsoft TV Technologies]","GetTag method","IDvbLinkageDescriptor.GetTag","IDvbLinkageDescriptor::GetTag","dvbsiparser/IDvbLinkageDescriptor::GetTag","mstv.idvblinkagedescriptor_gettag"]
old-location: mstv\idvblinkagedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 4a01430f-13b2-40ff-a47e-98e1bcdbf4fc
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IDvbLinkageDescriptor interface, IDvbLinkageDescriptor interface [Microsoft TV Technologies],GetTag method, IDvbLinkageDescriptor.GetTag, IDvbLinkageDescriptor::GetTag, dvbsiparser/IDvbLinkageDescriptor::GetTag, mstv.idvblinkagedescriptor_gettag
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
 - IDvbLinkageDescriptor::GetTag
 - dvbsiparser/IDvbLinkageDescriptor::GetTag
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
 - IDvbLinkageDescriptor.GetTag
---

# IDvbLinkageDescriptor::GetTag


## -description

Gets the tag that identifies a Digital Video Broadcast (DVB) linkage descriptor.

## -parameters

### -param pbVal [out]

Receives the identifier tag. For DVB linkage descriptors, this value is "0x4A".

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-idvblinkagedescriptor">IDvbLinkageDescriptor</a>