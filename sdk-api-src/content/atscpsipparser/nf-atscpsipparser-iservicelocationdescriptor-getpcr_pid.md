---
UID: NF:atscpsipparser.IServiceLocationDescriptor.GetPCR_PID
title: IServiceLocationDescriptor::GetPCR_PID (atscpsipparser.h)
description: Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.
helpviewer_keywords: ["GetPCR_PID","GetPCR_PID method [Microsoft TV Technologies]","GetPCR_PID method [Microsoft TV Technologies]","IServiceLocationDescriptor interface","IServiceLocationDescriptor interface [Microsoft TV Technologies]","GetPCR_PID method","IServiceLocationDescriptor.GetPCR_PID","IServiceLocationDescriptor::GetPCR_PID","atscpsipparser/IServiceLocationDescriptor::GetPCR_PID","mstv.iservicelocationdescriptor_getpcr_pid"]
old-location: mstv\iservicelocationdescriptor_getpcr_pid.htm
tech.root: mstv
ms.assetid: a81a2218-3c44-4b17-a5cb-bb68d10da977
ms.date: 12/05/2018
ms.keywords: GetPCR_PID, GetPCR_PID method [Microsoft TV Technologies], GetPCR_PID method [Microsoft TV Technologies],IServiceLocationDescriptor interface, IServiceLocationDescriptor interface [Microsoft TV Technologies],GetPCR_PID method, IServiceLocationDescriptor.GetPCR_PID, IServiceLocationDescriptor::GetPCR_PID, atscpsipparser/IServiceLocationDescriptor::GetPCR_PID, mstv.iservicelocationdescriptor_getpcr_pid
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
 - IServiceLocationDescriptor::GetPCR_PID
 - atscpsipparser/IServiceLocationDescriptor::GetPCR_PID
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
 - IServiceLocationDescriptor.GetPCR_PID
---

# IServiceLocationDescriptor::GetPCR_PID


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

Gets the program ID (PID) for the packets that contain the Program Clock Reference (PCR) in the transport stream from an Advanced Television Systems Committee (ATSC) Service Location Descriptor.

## -parameters

### -param pwVal [out]

Receives the PID value.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/atscpsipparser/nn-atscpsipparser-iservicelocationdescriptor">IServiceLocationDescriptor</a>