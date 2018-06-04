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

# IContinueCallback interface


## -description


Provides a generic callback mechanism for interruptible processes that should periodically ask an object whether to continue.

The <a href="https://msdn.microsoft.com/c84899df-fef1-473d-8278-d715a8ab8ee5">FContinue</a> method is a generic continuation request. <a href="https://msdn.microsoft.com/9031809a-8e5b-48d9-8af9-4a1a07532406">FContinuePrinting</a> carries extra information pertaining to a printing process and is used in the context of <a href="https://msdn.microsoft.com/eb0d15c0-8a34-4211-b840-29d5862cf767">IPrint</a>.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IContinueCallback</b> interface inherits from the <a href="iunknown.htm">IUnknown</a> interface. <b>IContinueCallback</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IContinueCallback</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c84899df-fef1-473d-8278-d715a8ab8ee5">FContinue</a>
</td>
<td align="left" width="63%">
Indicates whether a generic operation should continue.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/9031809a-8e5b-48d9-8af9-4a1a07532406">FContinuePrinting</a>
</td>
<td align="left" width="63%">
Indicates whether a lengthy printing operation should continue.

</td>
</tr>
</table> 

