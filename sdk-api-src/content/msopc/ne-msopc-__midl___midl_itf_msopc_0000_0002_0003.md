---
UID: NE:msopc.__MIDL___MIDL_itf_msopc_0000_0002_0003
title: "__MIDL___MIDL_itf_msopc_0000_0002_0003"
author: windows-driver-content
description: Describes the read/write status of a stream.
old-location: opc\opc_stream_io_mode.htm
old-project: OPC
ms.assetid: cf72ddcf-5472-451f-bfa8-94f549dc9246
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: OPC_STREAM_IO_MODE, OPC_STREAM_IO_MODE enumeration [Open Packaging Conventions], OPC_STREAM_IO_READ, OPC_STREAM_IO_WRITE, __MIDL___MIDL_itf_msopc_0000_0002_0003, msopc/OPC_STREAM_IO_MODE, msopc/OPC_STREAM_IO_READ, msopc/OPC_STREAM_IO_WRITE, opc.opc_stream_io_mode
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
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
req.typenames: OPC_STREAM_IO_MODE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	msopc.h
api_name:
-	OPC_STREAM_IO_MODE
product: Windows
targetos: Windows
req.lib: Msi.lib
req.dll: Msi.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# __MIDL___MIDL_itf_msopc_0000_0002_0003 enumeration


## -description


Describes the read/write status of a stream.


## -enum-fields




### -field OPC_STREAM_IO_READ

Creates a read-only stream for loading an existing package.


### -field OPC_STREAM_IO_WRITE

Creates a write-only stream for saving a new package.


## -remarks



<div class="alert"><b>Important</b>  <p class="note">Reading and writing to the same package is not recommended and may result in undefined behavior.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/ef392c88-49cd-4ffa-b1fb-1501c6448264">Getting Started with the Packaging API</a>



<a href="https://msdn.microsoft.com/d41bb51d-127c-4b24-8c93-4224404e0b2d">IOpcFactory::CreateStreamOnFile</a>



<b>Overviews</b>



<a href="https://msdn.microsoft.com/cb35d87e-bbec-42d3-9f9d-d1cf36f39419">Packaging API Programming Guide</a>



<a href="https://msdn.microsoft.com/885137be-35d5-4ec5-bbcc-16c95adf55ab">Packaging API Samples</a>



<a href="https://msdn.microsoft.com/c84246dd-f34b-40ea-8530-f93483445533">Packaging Enumerations</a>



<a href="https://msdn.microsoft.com/a0e9f38f-ab35-4fc2-855c-ea21bf164223">Packaging Interfaces</a>



<b>Reference</b>
 

 

