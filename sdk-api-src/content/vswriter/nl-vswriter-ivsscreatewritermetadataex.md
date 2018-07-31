---
UID: NL:vswriter.IVssCreateWriterMetadataEx
title: IVssCreateWriterMetadataEx
author: windows-sdk-content
description: The IVssCreateWriterMetadataEx interface is a C++ (not COM) interface that defines a method to report any file sets that will be explicitly excluded when a shadow copy is created.
old-location: base\ivsscreatewritermetadataex.htm
old-project: VSS
ms.assetid: eec0a7ef-ad7c-4fb6-a101-573c2d0943c2
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IVssCreateWriterMetadataEx, IVssCreateWriterMetadataEx interface, IVssCreateWriterMetadataEx interface,described, base.ivsscreatewritermetadataex, vswriter/IVssCreateWriterMetadataEx
ms.prod: windows
ms.technology: windows-sdk
ms.topic: class
req.header: vswriter.h
req.include-header: Vss.h, VsWriter.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IVssCreateWriterMetadataEx
product: Windows
targetos: Windows
req.lib: VssApi.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IVssCreateWriterMetadataEx class


## -description


The 
<b>IVssCreateWriterMetadataEx</b> interface is a C++ (not COM) interface that defines a method to report any <a href="vssgloss_f.htm">file sets</a> that will be explicitly excluded when a shadow copy is created. This interface is used only in 
the <a href="https://msdn.microsoft.com/542d479a-695a-4b1f-94e7-f2ffa08440b7">CVssWriterEx::OnIdentifyEx</a> method.

The <b>IVssCreateWriterMetadataEx</b> interface inherits from the <a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a> interface and <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>.

<b>IVssCreateWriterMetadataEx</b> defines the following method.<table>
<tr>
<th>Method</th>
<th>Description</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/6be4c63c-c36a-4ff4-92b7-63b69a030b86">AddExcludeFilesFromSnapshot</a>
</td>
<td>Reports any <a href="vssgloss_f.htm">file sets</a> that will be explicitly excluded by the writer when a shadow copy is created.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/427ed302-c3b7-483a-aa48-da6fec1160a9">IVssCreateWriterMetadata</a>
 

 

