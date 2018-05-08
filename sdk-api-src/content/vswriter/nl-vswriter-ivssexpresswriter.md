---
UID: NL:vswriter.IVssExpressWriter
title: IVssExpressWriter
author: windows-driver-content
description: Defines methods to manage metadata for a VSS express writer.
old-location: base\ivssexpresswriter.htm
old-project: VSS
ms.assetid: debb0731-6e24-4320-8236-220e07ec37c3
ms.author: windowsdriverdev
ms.date: 4/17/2018
ms.keywords: IVssExpressWriter, IVssExpressWriter interface, IVssExpressWriter interface,described, base.ivssexpresswriter, vswriter/IVssExpressWriter
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: class
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
-	IVssExpressWriter
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssExpressWriter class


## -description


Defines methods to manage metadata for a VSS express writer.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExpressWriter</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssExpressWriter</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExpressWriter</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/254f4a32-cb33-494e-8fb4-06ab1cc2b184">CreateMetadata</a>
</td>
<td align="left" width="63%">
Creates an express writer metadata object and returns an <a href="https://msdn.microsoft.com/49112cff-9e61-4218-a013-5ae5eb58b534">IVssCreateExpressWriterMetadata</a> interface pointer to it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/2b670278-4589-47b7-a9ad-a24187c39945">LoadMetadata</a>
</td>
<td align="left" width="63%">
Causes VSS to load the writer's metadata from a string instead of the express writer metadata store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/75cdc416-5fb6-4c9e-b7ab-f79b091786b2">Register</a>
</td>
<td align="left" width="63%">
Causes VSS to store the writer's metadata in the express writer metadata store.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/24398ace-4e76-471b-ae04-d2005e09cb6a">Unregister</a>
</td>
<td align="left" width="63%">
Causes VSS to delete the writer's metadata from the express writer metadata store.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/c24a1046-50b0-4fec-88f9-3bbd6970982a">CreateVssExpressWriter</a>
 

 

