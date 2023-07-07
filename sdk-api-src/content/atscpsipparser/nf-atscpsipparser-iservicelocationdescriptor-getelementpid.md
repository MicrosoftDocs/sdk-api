---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetElementPID
title: IServiceLocationDescriptor::GetElementPID (atscpsipparser.h)
description: Gets the program ID (PID) that identifies an elementary stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.
helpviewer_keywords: ["GetElementPID","GetElementPID method [Microsoft TV Technologies]","GetElementPID method [Microsoft TV Technologies]","IServiceLocationDescriptor interface","IServiceLocationDescriptor interface [Microsoft TV Technologies]","GetElementPID method","IServiceLocationDescriptor.GetElementPID","IServiceLocationDescriptor::GetElementPID","atscpsipparser/IServiceLocationDescriptor::GetElementPID","mstv.iservicelocationdescriptor_getelementpid"]
old-location: mstv\iservicelocationdescriptor_getelementpid.htm
tech.root: mstv
ms.assetid: 97b6091b-cacb-4e69-8ca4-c9f4b70f6304
ms.date: 12/05/2018
ms.keywords: GetElementPID, GetElementPID method [Microsoft TV Technologies], GetElementPID method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetElementPID method, IServiceLocationDescriptor.GetElementPID, IServiceLocationDescriptor::GetElementPID, atscpsipparser/IServiceLocationDescriptor::GetElementPID, mstv.iservicelocationdescriptor_getelementpid
req.header: atscpsipparser.h
req.include-header: Atscpsipparser.idl
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
 - IServiceLocationDescriptor::GetElementPID
 - atscpsipparser/IServiceLocationDescriptor::GetElementPID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - atscpsipparser.h
api_name:
 - IServiceLocationDescriptor.GetElementPID
---

# IServiceLocationDescriptor::GetElementPID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the program ID (PID) that identifies an elementary stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.

## -parameters

### -param bIndex [in]

Specifies the elementary stream,
  indexed from zero. Call the <a href="/previous-versions/windows/desktop/api/atscpsipparser/nf-atscpsipparser-iservicelocationdescriptor-getnumberofelements">IServiceLocationDescriptor::GetNumberOfElements</a> method to get the number of elementary streams in the descriptor.

### -param pwVal [out]

Receives the PID value for the elementary stream.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iservicelocationdescriptor">IServiceLocationDescriptor</a>