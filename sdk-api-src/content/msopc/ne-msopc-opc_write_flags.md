---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0005
title: OPC_WRITE_FLAGS (msopc.h)
description: Describes the encoding method that is used by the serialization object to produce the package.
helpviewer_keywords: ["OPC_WRITE_DEFAULT","OPC_WRITE_FLAGS","OPC_WRITE_FLAGS enumeration [Open Packaging Conventions]","OPC_WRITE_FORCE_ZIP32","msopc/OPC_WRITE_DEFAULT","msopc/OPC_WRITE_FLAGS","msopc/OPC_WRITE_FORCE_ZIP32","opc.opc_write_flags"]
old-location: opc\opc_write_flags.htm
tech.root: OPC
ms.assetid: 12006b4a-98e1-4761-bce3-32b83b54a2cb
ms.date: 12/05/2018
ms.keywords: OPC_WRITE_DEFAULT, OPC_WRITE_FLAGS, OPC_WRITE_FLAGS enumeration [Open Packaging Conventions], OPC_WRITE_FORCE_ZIP32, msopc/OPC_WRITE_DEFAULT, msopc/OPC_WRITE_FLAGS, msopc/OPC_WRITE_FORCE_ZIP32, opc.opc_write_flags
req.header: msopc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Opcobjectmodel.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: OPC_WRITE_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0000_0002_0005
 - msopc/__MIDL___MIDL_itf_msopc_0000_0002_0005
 - OPC_WRITE_FLAGS
 - msopc/OPC_WRITE_FLAGS
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
 - OPC_WRITE_FLAGS
---

# OPC_WRITE_FLAGS enumeration


## -description

Describes the encoding method that is used by the serialization object to produce the package.

## -enum-fields

### -field OPC_WRITE_DEFAULT:0

Use Zip64 encoding. The minimum software version for extracting a package with Zip64 encoding is 4.5.

### -field OPC_WRITE_FORCE_ZIP32:0x1

Force Zip32 encoding. The minimum software version for extracting a package with Zip32 encoding is 2.0.

If   one or more of the following Zip32 limitations are violated, the package write will fail:<ul>
<li>The maximum size for a single, uncompressed file item is 4 gigabytes.</li>
<li>The maximum number of file items is 65535 (2¹⁶-1).</li>
</ul>

## -see-also

<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-writepackagetostream">IOpcFactory::WritePackageToStream</a>



<a href="/previous-versions/windows/desktop/opc/open-packaging-conventions-overview">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>



<a href="/previous-versions/windows/desktop/opc/relationships-overview">Relationships Overview</a>
