---
UID: NL:vswriter.IVssCreateExpressWriterMetadata
title: IVssCreateExpressWriterMetadata
author: windows-sdk-content
description: The IVssCreateExpressWriterMetadata interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.
old-location: base\ivsscreateexpresswritermetadata.htm
old-project: vss
ms.assetid: 49112cff-9e61-4218-a013-5ae5eb58b534
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IVssCreateExpressWriterMetadata, IVssCreateExpressWriterMetadata interface, IVssCreateExpressWriterMetadata interface,described, base.ivsscreateexpresswritermetadata, vswriter/IVssCreateExpressWriterMetadata
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
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
tech.root: 
req.typenames: VSS_WRITERRESTORE_ENUM
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - VssApi.lib
 - VssApi.dll
api_name:
 - IVssCreateExpressWriterMetadata
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateExpressWriterMetadata class


## -description


The <b>IVssCreateExpressWriterMetadata</b> interface is a COM interface containing methods to construct the Writer Metadata Document for an express writer.

After it is constructed, the Writer Metadata Document is a read-only object that requesters query for information about a writer and its components.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssCreateExpressWriterMetadata</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IVssCreateExpressWriterMetadata</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssCreateExpressWriterMetadata</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e17ed040-7fe2-4605-b1b5-295abbf14289">AddComponent</a>
</td>
<td align="left" width="63%">
Adds a 
    file group to an express writer's set of components to be backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/1d7e28de-8bb7-4ab4-bcdd-554d47007233">AddComponentDependency</a>
</td>
<td align="left" width="63%">
Allows an express writer to indicate that a component it manages has an explicit writer-component dependency; that is, another component (possibly managed by another writer) must be backed up and restored with it.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a8d0d6bc-456a-405e-abd9-5ab4b2a59e63">AddExcludeFiles</a>
</td>
<td align="left" width="63%">
Excludes a file set (a specified file or files) that might otherwise be implicitly included when a component of an express writer is backed up.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9a3f409e-f58a-4c06-ad5e-b0a8bc03da2c">AddFilesToFileGroup</a>
</td>
<td align="left" width="63%">
Adds a file set (a specified file or files) to a specified file group component for an express writer.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c2a1ba98-74a1-4944-ac31-fec364060a75">SaveAsXML</a>
</td>
<td align="left" width="63%">
Stores the Writer Metadata Document that contains an express writer's state information into a specified string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b270424d-61e1-4984-a487-4dcb4e113985">SetBackupSchema</a>
</td>
<td align="left" width="63%">
Used by an express writer to indicate in its Writer Metadata Document the types of backup operations it can participate in.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/220e399b-aafd-4b72-bef4-abc3f39f202f">SetRestoreMethod</a>
</td>
<td align="left" width="63%">
Specifies how an express writer's data is to be restored.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a>



<a href="https://msdn.microsoft.com/debb0731-6e24-4320-8236-220e07ec37c3">IVssExpressWriter</a>
 

 

