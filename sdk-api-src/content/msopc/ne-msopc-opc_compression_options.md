---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0002
title: OPC_COMPRESSION_OPTIONS (msopc.h)
description: Describes ways to compress part content.
helpviewer_keywords: ["OPC_COMPRESSION_FAST","OPC_COMPRESSION_MAXIMUM","OPC_COMPRESSION_NONE","OPC_COMPRESSION_NORMAL","OPC_COMPRESSION_OPTIONS","OPC_COMPRESSION_OPTIONS enumeration [Open Packaging Conventions]","OPC_COMPRESSION_SUPERFAST","msopc/OPC_COMPRESSION_FAST","msopc/OPC_COMPRESSION_MAXIMUM","msopc/OPC_COMPRESSION_NONE","msopc/OPC_COMPRESSION_NORMAL","msopc/OPC_COMPRESSION_OPTIONS","msopc/OPC_COMPRESSION_SUPERFAST","opc.opc_compression_options"]
old-location: opc\opc_compression_options.htm
tech.root: OPC
ms.assetid: bc821e84-fd18-449c-89d0-a261f43f8971
ms.date: 12/05/2018
ms.keywords: OPC_COMPRESSION_FAST, OPC_COMPRESSION_MAXIMUM, OPC_COMPRESSION_NONE, OPC_COMPRESSION_NORMAL, OPC_COMPRESSION_OPTIONS, OPC_COMPRESSION_OPTIONS enumeration [Open Packaging Conventions], OPC_COMPRESSION_SUPERFAST, msopc/OPC_COMPRESSION_FAST, msopc/OPC_COMPRESSION_MAXIMUM, msopc/OPC_COMPRESSION_NONE, msopc/OPC_COMPRESSION_NORMAL, msopc/OPC_COMPRESSION_OPTIONS, msopc/OPC_COMPRESSION_SUPERFAST, opc.opc_compression_options
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcbase.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPC_COMPRESSION_OPTIONS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0000_0002_0002
 - msopc/__MIDL___MIDL_itf_msopc_0000_0002_0002
 - OPC_COMPRESSION_OPTIONS
 - msopc/OPC_COMPRESSION_OPTIONS
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
 - OPC_COMPRESSION_OPTIONS
---

# OPC_COMPRESSION_OPTIONS enumeration


## -description

Describes ways to compress   part content.

## -enum-fields

### -field OPC_COMPRESSION_NONE:-1

Compression is turned off.

### -field OPC_COMPRESSION_NORMAL:0

Compression is optimized for a balance between size and performance.

### -field OPC_COMPRESSION_MAXIMUM:1

Compression is optimized for size.

### -field OPC_COMPRESSION_FAST:2

Compression is optimized for performance.

### -field OPC_COMPRESSION_SUPERFAST:3

Compression is optimized for high performance.

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpart-getcompressionoptions">IOpcPart::GetCompressionOptions</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcpartset-createpart">IOpcPartSet::CreatePart</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
