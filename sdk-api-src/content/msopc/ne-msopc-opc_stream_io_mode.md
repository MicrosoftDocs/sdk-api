---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0003
title: OPC_STREAM_IO_MODE (msopc.h)
description: Describes the read/write status of a stream.
helpviewer_keywords: ["OPC_STREAM_IO_MODE","OPC_STREAM_IO_MODE enumeration [Open Packaging Conventions]","OPC_STREAM_IO_READ","OPC_STREAM_IO_WRITE","msopc/OPC_STREAM_IO_MODE","msopc/OPC_STREAM_IO_READ","msopc/OPC_STREAM_IO_WRITE","opc.opc_stream_io_mode"]
old-location: opc\opc_stream_io_mode.htm
tech.root: OPC
ms.assetid: cf72ddcf-5472-451f-bfa8-94f549dc9246
ms.date: 12/05/2018
ms.keywords: OPC_STREAM_IO_MODE, OPC_STREAM_IO_MODE enumeration [Open Packaging Conventions], OPC_STREAM_IO_READ, OPC_STREAM_IO_WRITE, msopc/OPC_STREAM_IO_MODE, msopc/OPC_STREAM_IO_READ, msopc/OPC_STREAM_IO_WRITE, opc.opc_stream_io_mode
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msopc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPC_STREAM_IO_MODE
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0000_0002_0003
 - msopc/__MIDL___MIDL_itf_msopc_0000_0002_0003
 - OPC_STREAM_IO_MODE
 - msopc/OPC_STREAM_IO_MODE
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_STREAM_IO_MODE
---

# OPC_STREAM_IO_MODE enumeration


## -description

Describes the read/write status of a stream.

## -enum-fields

### -field OPC_STREAM_IO_READ:1

Creates a read-only stream for loading an existing package.

### -field OPC_STREAM_IO_WRITE:2

Creates a write-only stream for saving a new package.

## -remarks

<div class="alert"><b>Important</b>  <p class="note">Reading and writing to the same package is not recommended and may result in undefined behavior.

</div>
<div> </div>

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-createstreamonfile">IOpcFactory::CreateStreamOnFile</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
