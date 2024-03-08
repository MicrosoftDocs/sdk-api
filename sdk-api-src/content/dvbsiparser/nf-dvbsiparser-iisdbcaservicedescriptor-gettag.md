---
UID: NF:dvbsiparser.IIsdbCAServiceDescriptor.GetTag
title: IIsdbCAServiceDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a conditional access (CA) service descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbCAServiceDescriptor interface","IIsdbCAServiceDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbCAServiceDescriptor.GetTag","IIsdbCAServiceDescriptor::GetTag","dvbsiparser/IIsdbCAServiceDescriptor::GetTag","mstv.iisdbcaservicedescriptor_gettag"]
old-location: mstv\iisdbcaservicedescriptor_gettag.htm
tech.root: mstv
ms.assetid: 55f7b955-03f6-4c40-bd73-175bf3453ed0
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbCAServiceDescriptor interface, IIsdbCAServiceDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbCAServiceDescriptor.GetTag, IIsdbCAServiceDescriptor::GetTag, dvbsiparser/IIsdbCAServiceDescriptor::GetTag, mstv.iisdbcaservicedescriptor_gettag
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
 - IIsdbCAServiceDescriptor::GetTag
 - dvbsiparser/IIsdbCAServiceDescriptor::GetTag
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
 - IIsdbCAServiceDescriptor.GetTag
---

# IIsdbCAServiceDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a conditional access (CA) service descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For conditional access service descriptors, this value is 0xCC.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcaservicedescriptor">IIsdbCAServiceDescriptor</a>