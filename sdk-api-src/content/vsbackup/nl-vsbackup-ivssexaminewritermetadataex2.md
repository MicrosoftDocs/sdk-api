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

# IVssExamineWriterMetadataEx2 class


## -description


Defines methods to retrieve version information and other basic information for a specific writer instance.

Your writer application should implement this interface only if you need to use the <a href="https://msdn.microsoft.com/77f21feb-bd7c-4fd0-820b-9dabb1bcbc89">GetExcludeFromSnapshotCount</a>, <a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">GetExcludeFromSnapshotFile</a>, and <a href="https://msdn.microsoft.com/d702263e-0ea5-428c-bbd6-1ab8a7334a92">GetVersion</a> methods. Otherwise, your writer application should implement  the <a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a> interface or the <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface instead.

The <b>IVssExamineWriterMetadataEx2</b> interface is a C++ (not COM) interface.

To obtain an instance of the <b>IVssExamineWriterMetadataEx2</b> 
   interface, call the <a href="_com_iunknown_queryinterface">QueryInterface</a> method of the 
   <a href="https://msdn.microsoft.com/b3aa04d9-7299-4e3a-b092-d07f2de6eefe">IVssExamineWriterMetadata</a> interface, and pass  
   the <b>IID_IVssExamineWriterMetadataEx2</b> constant as the interface identifier (IID) parameter.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IVssExamineWriterMetadataEx2</b> interface inherits from <a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a>. <b>IVssExamineWriterMetadataEx2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IVssExamineWriterMetadataEx2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/77f21feb-bd7c-4fd0-820b-9dabb1bcbc89">GetExcludeFromSnapshotCount</a>
</td>
<td align="left" width="63%">
Obtains the number of <a href="vssgloss_f.htm">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3df57749-9a26-4187-b1fc-aeb68a4d1d06">GetExcludeFromSnapshotFile</a>
</td>
<td align="left" width="63%">
Obtains information about <a href="vssgloss_f.htm">file sets</a> that have been explicitly excluded from a given shadow copy.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d702263e-0ea5-428c-bbd6-1ab8a7334a92">GetVersion</a>
</td>
<td align="left" width="63%">
Obtains the version information for a writer application.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/363c987c-7d6c-4efe-988a-1b288f9b4d3c">IVssExamineWriterMetadataEx</a>
 

 

