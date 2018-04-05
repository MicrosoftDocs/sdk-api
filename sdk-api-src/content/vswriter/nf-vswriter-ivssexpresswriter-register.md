---
UID: NF:vswriter.IVssExpressWriter.Register
title: IVssExpressWriter::Register method
author: windows-driver-content
description: Causes VSS to store the writer's metadata in the express writer metadata store.
old-location: base\ivssexpresswriter_register.htm
old-project: VSS
ms.assetid: 75cdc416-5fb6-4c9e-b7ab-f79b091786b2
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IVssExpressWriter, IVssExpressWriter interface, Register method, IVssExpressWriter::Register, Register method, Register method, IVssExpressWriter interface, Register,IVssExpressWriter.Register, base.ivssexpresswriter_register, vswriter/IVssExpressWriter::Register
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: vswriter.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	VsWriter.h
api_name:
-	IVssExpressWriter.Register
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExpressWriter::Register method


## -description


Causes VSS to store the writer's metadata in the express writer metadata store.


## -parameters






## -returns



The following are the valid return codes for this method.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
<dt>0x00000000L</dt>
</dl>
</td>
<td width="60%">
The operation was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>VSS_E_OBJECT_ALREADY_EXISTS</b></dt>
<dt>0x8004230DL</dt>
</dl>
</td>
<td width="60%">
Metadata has already been stored for this writer.

</td>
</tr>
</table>
 




## -remarks



Before using this method, the caller must have either used the <a href="https://msdn.microsoft.com/2b670278-4589-47b7-a9ad-a24187c39945">LoadMetadata</a> method to load the writer's metadata directly or used the <a href="https://msdn.microsoft.com/254f4a32-cb33-494e-8fb4-06ab1cc2b184">CreateMetadata</a> method to create a writer metadata object.




## -see-also




<a href="https://msdn.microsoft.com/debb0731-6e24-4320-8236-220e07ec37c3">IVssExpressWriter</a>
 

 

