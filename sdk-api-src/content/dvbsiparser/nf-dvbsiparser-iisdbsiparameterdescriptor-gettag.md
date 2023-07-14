---
UID: NF:dvbsiparser.IIsdbSIParameterDescriptor.GetTag
title: IIsdbSIParameterDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a service information (SI) parameter descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbSIParameterDescriptor interface","IIsdbSIParameterDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbSIParameterDescriptor.GetTag","IIsdbSIParameterDescriptor::GetTag","dvbsiparser/IIsdbSIParameterDescriptor::GetTag","mstv.iisdbsiparameterdescriptor_gettag"]
old-location: mstv\iisdbsiparameterdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 9d38b158-39b0-4960-b392-086595680133
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbSIParameterDescriptor interface, IIsdbSIParameterDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbSIParameterDescriptor.GetTag, IIsdbSIParameterDescriptor::GetTag, dvbsiparser/IIsdbSIParameterDescriptor::GetTag, mstv.iisdbsiparameterdescriptor_gettag
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
 - IIsdbSIParameterDescriptor::GetTag
 - dvbsiparser/IIsdbSIParameterDescriptor::GetTag
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
 - IIsdbSIParameterDescriptor.GetTag
---

# IIsdbSIParameterDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a service information (SI) parameter descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For SI parameter descriptors, this value is 0xD7.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbsiparameterdescriptor">IIsdbSIParameterDescriptor</a>