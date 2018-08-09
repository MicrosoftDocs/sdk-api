---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0005
title: "__MIDL___MIDL_itf_msopc_0000_0002_0005"
author: windows-sdk-content
description: Describes the encoding method that is used by the serialization object to produce the package.
old-location: opc\opc_write_flags.htm
old-project: OPC
ms.assetid: 12006b4a-98e1-4761-bce3-32b83b54a2cb
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: OPC_WRITE_DEFAULT, OPC_WRITE_FLAGS, OPC_WRITE_FLAGS enumeration [Open Packaging Conventions], OPC_WRITE_FORCE_ZIP32, __MIDL___MIDL_itf_msopc_0000_0002_0005, msopc/OPC_WRITE_DEFAULT, msopc/OPC_WRITE_FLAGS, msopc/OPC_WRITE_FORCE_ZIP32, opc.opc_write_flags
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
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
tech.root: 
req.typenames: OPC_WRITE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - msopc.h
api_name:
 - OPC_WRITE_FLAGS
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msopc_0000_0002_0005 enumeration


## -description


Describes the encoding method that is used by the serialization object to produce the package.


## -enum-fields




### -field OPC_WRITE_DEFAULT

Use Zip64 encoding. The minimum software version for extracting a package with Zip64 encoding is 4.5.


### -field OPC_WRITE_FORCE_ZIP32

Force Zip32 encoding. The minimum software version for extracting a package with Zip32 encoding is 2.0.

If   one or more of the following Zip32 limitations are violated, the package write will fail:<ul>
<li>The maximum size for a single, uncompressed file item is 4 gigabytes.</li>
<li>The maximum number of file items is 65535 (2¹⁶-1).</li>
</ul>



## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/b155700d-3037-4c6e-b2f2-bba39513d7d3">IOpcFactory::WritePackageToStream</a>



<a href="https://msdn.microsoft.com/115430f2-8e1f-46ba-ae6e-b7f3689048ff">Open Packaging Conventions Fundamentals</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/8e071847-7eb2-4528-8402-4aaa1f5cd216">Relationships Overview</a>
 

 

