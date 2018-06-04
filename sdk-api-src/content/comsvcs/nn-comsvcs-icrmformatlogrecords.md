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

# ICrmFormatLogRecords interface


## -description


Converts the log records to viewable format so that they can be presented using a generic monitoring tool.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICrmFormatLogRecords</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ICrmFormatLogRecords</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ICrmFormatLogRecords</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5234f582-88e2-4a9a-8650-d0d2d4b39f31">GetColumn</a>
</td>
<td align="left" width="63%">
Formats one unstructured log record into an array of viewable fields.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/d1b1bc24-6e9d-4f48-ac11-f3892a3be2b1">GetColumnCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of fields (columns) in a log record of the type used by this CRM Compensator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b7ca50f9-7e42-4cde-9985-0501ae34f040">GetColumnHeaders</a>
</td>
<td align="left" width="63%">
Retrieves the names of the fields (columns).

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f2681fe3-744b-4172-8908-1d823d2e2371">GetColumnVariants</a>
</td>
<td align="left" width="63%">
Formats one structured log record into an array of viewable fields.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/3d490da6-1577-4a77-9f7d-6188f96f2914">COM+ Compensating Resource Manager</a>
 

 

