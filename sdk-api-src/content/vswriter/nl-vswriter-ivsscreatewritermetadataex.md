---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
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
 

 

