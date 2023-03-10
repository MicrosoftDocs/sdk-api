---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0004
title: OPC_READ_FLAGS (msopc.h)
description: Describes the read settings for caching package components and validating them against ECMA-376 OpenXML, 1st Edition, Part 2:\_Open Packaging Conventions (OPC) conformance requirements.
helpviewer_keywords: ["OPC_CACHE_ON_ACCESS","OPC_READ_DEFAULT","OPC_READ_FLAGS","OPC_READ_FLAGS enumeration [Open Packaging Conventions]","OPC_VALIDATE_ON_LOAD","msopc/OPC_CACHE_ON_ACCESS","msopc/OPC_READ_DEFAULT","msopc/OPC_READ_FLAGS","msopc/OPC_VALIDATE_ON_LOAD","opc.opc_read_flags"]
old-location: opc\opc_read_flags.htm
tech.root: OPC
ms.assetid: f7d21dac-c606-4a6a-9d6a-cf6f8ec4dbb5
ms.date: 12/05/2018
ms.keywords: OPC_CACHE_ON_ACCESS, OPC_READ_DEFAULT, OPC_READ_FLAGS, OPC_READ_FLAGS enumeration [Open Packaging Conventions], OPC_VALIDATE_ON_LOAD, msopc/OPC_CACHE_ON_ACCESS, msopc/OPC_READ_DEFAULT, msopc/OPC_READ_FLAGS, msopc/OPC_VALIDATE_ON_LOAD, opc.opc_read_flags
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
req.typenames: OPC_READ_FLAGS
req.redist: 
ms.custom: 19H1
f1_keywords:
 - __MIDL___MIDL_itf_msopc_0000_0002_0004
 - msopc/__MIDL___MIDL_itf_msopc_0000_0002_0004
 - OPC_READ_FLAGS
 - msopc/OPC_READ_FLAGS
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
 - OPC_READ_FLAGS
---

# OPC_READ_FLAGS enumeration


## -description

Describes the read settings for caching package components and validating them against <i>ECMA-376 OpenXML, 1st Edition, Part 2: Open Packaging Conventions (OPC)</i> conformance requirements.

## -enum-fields

### -field OPC_READ_DEFAULT:0

Validate a package component against <i>OPC</i> conformance requirements when the  component is accessed. For more information about <i>OPC</i> conformance validation, see Remarks.

When validation is performed on access, <i>OPC</i> validation errors can be returned by any method.

### -field OPC_VALIDATE_ON_LOAD:0x1

Validate all package components against <i>OPC</i> conformance requirements when a package is loaded. For more information about <i>OPC</i> conformance validation, see Remarks.

If this setting is enabled, performance costs for loading and validating package components are paid when the package is first loaded.

### -field OPC_CACHE_ON_ACCESS:0x2

Cache decompressed package component data as a temp file when accessing the component for the first time. When a  package component is accessed repeatedly, this caching reduces overhead because the component data is decompressed one time for the first read instead of once for every read operation.

## -remarks

If both the <b>OPC_CACHE_ON_ACCESS</b> and <b>OPC_VALIDATE_ON_LOAD</b> read flags are set, all package components are decompressed and cached when a package is loaded.

The Packaging APIs do not use the <i>OPC</i> core properties feature; therefore, the core properties requirements listed in Table H-9 of the <i>OPC</i> are not validated by the Packaging APIs. For more information about <i>OPC</i> conformance requirements, see 1st edition, Part 2: Open Packaging Conventions in <a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML</a>  (http://www.ecma-international.org/publications/standards/Ecma-376.htm).

<div class="alert"><b>Important</b>  Parts may be repeatedly read from the stream at any time, regardless of which read flags are set. For example, when a package is saved, previously accessed relationships in a Relationships part in the original package may be accessed again to preserve markup compatibility.</div>
<div> </div>

## -see-also

<a href="https://www.ecma-international.org/publications/standards/Ecma-376.htm">ECMA-376 OpenXML standard</a>



<b>External Resources</b>



<a href="/previous-versions/windows/desktop/opc/packaging-api-overview">Getting Started with the Packaging API</a>



<a href="/previous-versions/windows/desktop/api/msopc/nf-msopc-iopcfactory-readpackagefromstream">IOpcFactory::ReadPackageFromStream</a>



<b>Overviews</b>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-guide">Packaging API Programming Guide</a>



<a href="/previous-versions/windows/desktop/opc/packaging-programming-samples">Packaging API Samples</a>



<a href="/previous-versions/windows/desktop/opc/packaging-enumerations">Packaging Enumerations</a>



<a href="/previous-versions/windows/desktop/legacy/dd371635(v=vs.85)">Packaging Interfaces</a>



<b>Reference</b>
