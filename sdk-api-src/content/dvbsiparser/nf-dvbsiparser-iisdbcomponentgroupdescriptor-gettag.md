---
UID: NF:dvbsiparser.IIsdbComponentGroupDescriptor.GetTag
title: IIsdbComponentGroupDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) component group descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbComponentGroupDescriptor interface","IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbComponentGroupDescriptor.GetTag","IIsdbComponentGroupDescriptor::GetTag","dvbsiparser/IIsdbComponentGroupDescriptor::GetTag","mstv.iisdbcomponentgroupdescriptor_gettag"]
old-location: mstv\iisdbcomponentgroupdescriptor_gettag.htm
tech.root: mstv
ms.assetid: ec33ae30-2e17-4db3-9c08-99447e05686c
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbComponentGroupDescriptor interface, IIsdbComponentGroupDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbComponentGroupDescriptor.GetTag, IIsdbComponentGroupDescriptor::GetTag, dvbsiparser/IIsdbComponentGroupDescriptor::GetTag, mstv.iisdbcomponentgroupdescriptor_gettag
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
 - IIsdbComponentGroupDescriptor::GetTag
 - dvbsiparser/IIsdbComponentGroupDescriptor::GetTag
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
 - IIsdbComponentGroupDescriptor.GetTag
---

# IIsdbComponentGroupDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies an Integrated Services Digital Broadcasting (ISDB) component group descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For ISDB component group descriptors, this value is 0xD9.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbcomponentgroupdescriptor">IIsdbComponentGroupDescriptor</a>