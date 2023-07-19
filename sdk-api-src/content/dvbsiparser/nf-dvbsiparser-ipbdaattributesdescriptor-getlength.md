---
UID: NF:dvbsiparser.IPBDAAttributesDescriptor.GetLength
title: IPBDAAttributesDescriptor::GetLength (dvbsiparser.h)
description: Gets the length of a Protected Broadcast Driver Architecture (PBDA) attributes descriptor from a Protected Broadcast Device Architecture (PBDA) transport stream, in bytes.
helpviewer_keywords: ["GetLength","GetLength method [Microsoft TV Technologies]","GetLength method [Microsoft TV Technologies]","IPBDAAttributesDescriptor interface","IPBDAAttributesDescriptor interface [Microsoft TV Technologies]","GetLength method","IPBDAAttributesDescriptor.GetLength","IPBDAAttributesDescriptor::GetLength","dvbsiparser/IPBDAAttributesDescriptor::GetLength","mstv.ipbdaattributesdescriptor_getlength"]
old-location: mstv\ipbdaattributesdescriptor_getlength.htm
tech.root: mstv
ms.assetid: b18ebaa1-aca4-4d21-adb7-d233e18cd320
ms.date: 12/05/2018
ms.keywords: GetLength, GetLength method [Microsoft TV Technologies], GetLength method [Microsoft TV Technologies],IPBDAAttributesDescriptor interface, IPBDAAttributesDescriptor interface [Microsoft TV Technologies],GetLength method, IPBDAAttributesDescriptor.GetLength, IPBDAAttributesDescriptor::GetLength, dvbsiparser/IPBDAAttributesDescriptor::GetLength, mstv.ipbdaattributesdescriptor_getlength
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
 - IPBDAAttributesDescriptor::GetLength
 - dvbsiparser/IPBDAAttributesDescriptor::GetLength
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
 - IPBDAAttributesDescriptor.GetLength
---

# IPBDAAttributesDescriptor::GetLength


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the length of a Protected Broadcast Driver Architecture (PBDA) attributes descriptor from a Protected Broadcast  Device Architecture (PBDA) transport stream, in bytes.

## -parameters

### -param pwVal [out]

Receives the descriptor length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdaattributesdescriptor">IPBDAAttributesDescriptor</a>