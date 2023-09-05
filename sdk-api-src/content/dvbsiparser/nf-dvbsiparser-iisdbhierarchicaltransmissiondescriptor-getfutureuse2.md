---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetFutureUse2
title: IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2 (dvbsiparser.h)
description: Gets the value of the 3-bit reserved_future_use field from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor.
helpviewer_keywords: ["GetFutureUse2","GetFutureUse2 method [Microsoft TV Technologies]","GetFutureUse2 method [Microsoft TV Technologies]","IIsdbHierarchicalTransmissionDescriptor interface","IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies]","GetFutureUse2 method","IIsdbHierarchicalTransmissionDescriptor.GetFutureUse2","IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2","dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2","mstv.iisdbhierarchicaltransmissiondescriptor_getfutureuse2"]
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_getfutureuse2.htm
tech.root: mstv
ms.assetid: 19404536-3104-4ac7-a979-73236007d553
ms.date: 12/05/2018
ms.keywords: GetFutureUse2, GetFutureUse2 method [Microsoft TV Technologies], GetFutureUse2 method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetFutureUse2 method, IIsdbHierarchicalTransmissionDescriptor.GetFutureUse2, IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2, mstv.iisdbhierarchicaltransmissiondescriptor_getfutureuse2
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
 - IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2
 - dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2
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
 - IIsdbHierarchicalTransmissionDescriptor.GetFutureUse2
---

# IIsdbHierarchicalTransmissionDescriptor::GetFutureUse2


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the value of the 3-bit reserved_future_use field from an Integrated Services Digital Broadcasting (ISDB) hierarchical transmission descriptor.

## -parameters

### -param pbVal [out]

Receives the 3-bit reserved_future_use field value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbhierarchicaltransmissiondescriptor">IIsdbHierarchicalTransmissionDescriptor</a>