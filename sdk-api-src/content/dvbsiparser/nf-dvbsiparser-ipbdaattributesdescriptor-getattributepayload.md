---
UID: NF:dvbsiparser.IPBDAAttributesDescriptor.GetAttributePayload
title: IPBDAAttributesDescriptor::GetAttributePayload (dvbsiparser.h)
description: Gets the descriptor body from an attributes descriptor in a Protected Broadcast Device Architecture (PBDA) transport stream.
helpviewer_keywords: ["GetAttributePayload","GetAttributePayload method [Microsoft TV Technologies]","GetAttributePayload method [Microsoft TV Technologies]","IPBDAAttributesDescriptor interface","IPBDAAttributesDescriptor interface [Microsoft TV Technologies]","GetAttributePayload method","IPBDAAttributesDescriptor.GetAttributePayload","IPBDAAttributesDescriptor::GetAttributePayload","dvbsiparser/IPBDAAttributesDescriptor::GetAttributePayload","mstv.ipbdaattributesdescriptor_getattributepayload"]
old-location: mstv\ipbdaattributesdescriptor_getattributepayload.htm
tech.root: mstv
ms.assetid: 315f6afe-a5cc-4fe2-8029-fcf280b358b2
ms.date: 12/05/2018
ms.keywords: GetAttributePayload, GetAttributePayload method [Microsoft TV Technologies], GetAttributePayload method [Microsoft TV Technologies],IPBDAAttributesDescriptor interface, IPBDAAttributesDescriptor interface [Microsoft TV Technologies],GetAttributePayload method, IPBDAAttributesDescriptor.GetAttributePayload, IPBDAAttributesDescriptor::GetAttributePayload, dvbsiparser/IPBDAAttributesDescriptor::GetAttributePayload, mstv.ipbdaattributesdescriptor_getattributepayload
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
 - IPBDAAttributesDescriptor::GetAttributePayload
 - dvbsiparser/IPBDAAttributesDescriptor::GetAttributePayload
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
 - IPBDAAttributesDescriptor.GetAttributePayload
---

# IPBDAAttributesDescriptor::GetAttributePayload


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the descriptor body from an attributes descriptor in a Protected Broadcast  Device Architecture (PBDA) transport stream.

## -parameters

### -param ppbAttributeBuffer [out]

Pointer to a buffer that receives the descriptor body. The caller must free this memory after use.

### -param pdwAttributeLength [out]

Receives the descriptor body length.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-ipbdaattributesdescriptor">IPBDAAttributesDescriptor</a>