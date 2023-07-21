---
UID: NF:dvbsiparser.IPBDAAttributesDescriptor.GetTag
title: IPBDAAttributesDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that uniquely identifies an attributes descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IPBDAAttributesDescriptor interface","IPBDAAttributesDescriptor interface [Microsoft TV Technologies]","GetTag method","IPBDAAttributesDescriptor.GetTag","IPBDAAttributesDescriptor::GetTag","dvbsiparser/IPBDAAttributesDescriptor::GetTag","mstv.ipbdaattributesdescriptor_gettag"]
old-location: mstv\ipbdaattributesdescriptor_gettag.htm
tech.root: mstv
ms.assetid: 397e76b6-83f2-4d0c-87a0-0575aa746020
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IPBDAAttributesDescriptor interface, IPBDAAttributesDescriptor interface [Microsoft TV Technologies],GetTag method, IPBDAAttributesDescriptor.GetTag, IPBDAAttributesDescriptor::GetTag, dvbsiparser/IPBDAAttributesDescriptor::GetTag, mstv.ipbdaattributesdescriptor_gettag
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
 - IPBDAAttributesDescriptor::GetTag
 - dvbsiparser/IPBDAAttributesDescriptor::GetTag
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
 - IPBDAAttributesDescriptor.GetTag
---

# IPBDAAttributesDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that uniquely identifies an attributes descriptor in a Protected Broadcast Driver Architecture (PBDA) transport stream.

## -parameters

### -param pbVal [out]

Gets the tag value. For PBDA attributes descriptors, this value is 0x81.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdaattributesdescriptor">IPBDAAttributesDescriptor</a>