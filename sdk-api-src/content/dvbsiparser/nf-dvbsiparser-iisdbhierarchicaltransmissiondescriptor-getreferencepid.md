---
UID: NF:dvbsiparser.IIsdbHierarchicalTransmissionDescriptor.GetReferencePid
title: IIsdbHierarchicalTransmissionDescriptor::GetReferencePid (dvbsiparser.h)
description: Gets the program ID (PID) of the primary hierarchical stream from a hierarchical transmission descriptor.
helpviewer_keywords: ["GetReferencePid","GetReferencePid method [Microsoft TV Technologies]","GetReferencePid method [Microsoft TV Technologies]","IIsdbHierarchicalTransmissionDescriptor interface","IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies]","GetReferencePid method","IIsdbHierarchicalTransmissionDescriptor.GetReferencePid","IIsdbHierarchicalTransmissionDescriptor::GetReferencePid","dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetReferencePid","mstv.iisdbhierarchicaltransmissiondescriptor_getreferencepid"]
old-location: mstv\iisdbhierarchicaltransmissiondescriptor_getreferencepid.htm
tech.root: mstv
ms.assetid: 4c1d96eb-e2d6-4f3a-8a3c-88c0d920ad44
ms.date: 12/05/2018
ms.keywords: GetReferencePid, GetReferencePid method [Microsoft TV Technologies], GetReferencePid method [Microsoft TV Technologies],IIsdbHierarchicalTransmissionDescriptor interface, IIsdbHierarchicalTransmissionDescriptor interface [Microsoft TV Technologies],GetReferencePid method, IIsdbHierarchicalTransmissionDescriptor.GetReferencePid, IIsdbHierarchicalTransmissionDescriptor::GetReferencePid, dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetReferencePid, mstv.iisdbhierarchicaltransmissiondescriptor_getreferencepid
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
 - IIsdbHierarchicalTransmissionDescriptor::GetReferencePid
 - dvbsiparser/IIsdbHierarchicalTransmissionDescriptor::GetReferencePid
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
 - IIsdbHierarchicalTransmissionDescriptor.GetReferencePid
---

# IIsdbHierarchicalTransmissionDescriptor::GetReferencePid


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the program ID (PID) of the primary hierarchical stream from a hierarchical transmission descriptor.

## -parameters

### -param pwVal [out]

Receives the PID value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/dvbsiparser/nn-dvbsiparser-iisdbhierarchicaltransmissiondescriptor">IIsdbHierarchicalTransmissionDescriptor</a>