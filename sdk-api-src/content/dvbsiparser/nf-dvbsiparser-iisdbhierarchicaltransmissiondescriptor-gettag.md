---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetTag
title: IIsdbHierarchicalTransmissionDescriptor::GetTag (dvbsiparser.h)
description: Gets the tag that identifies a hierarchical transmission descriptor.
helpviewer_keywords: ["GetTag","GetTag method [Microsoft TV Technologies]","GetTag method [Microsoft TV Technologies]","IIsdbHierarchicalTransmissionDescriptor interface","IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies]","GetTag method","IIsdbHierarchicalTransmissionDescriptor.GetTag","IIsdbHierarchicalTransmissionDescriptor::GetTag","dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetTag","mstv.iisdbhierarchicaltransmissiondescriptor_gettag"]
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_gettag.htm
tech.root: mstv
ms.assetid: 1aed2424-567b-4a6b-ae32-b3c74ce75026
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Microsoft TV Technologies], GetTag method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetTag method, IIsdbHierarchicalTransmissionDescriptor.GetTag, IIsdbHierarchicalTransmissionDescriptor::GetTag, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetTag, mstv.iisdbhierarchicaltransmissiondescriptor_gettag
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
 - IIsdbHierarchicalTransmissionDescriptor::GetTag
 - dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetTag
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
 - IIsdbHierarchicalTransmissionDescriptor.GetTag
---

# IIsdbHierarchicalTransmissionDescriptor::GetTag


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the tag that identifies a hierarchical transmission descriptor.

## -parameters

### -param pbVal [out]

Receives the tag value. For hierarchical transmission descriptors, this value is 0xC0.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbhierarchicaltransmissiondescriptor">IIsdbHierarchicalTransmissionDescriptor</a>