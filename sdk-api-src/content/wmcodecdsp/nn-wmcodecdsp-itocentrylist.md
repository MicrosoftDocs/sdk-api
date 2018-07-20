---
UID: NN:wmcodecdsp.ITocEntryList
title: ITocEntryList
author: windows-sdk-content
description: The ITocEntryList interface represents a list of entries in a table of contents. It provides methods for adding entries to, and removing entries from the list.
old-location: mf\itocentrylist.htm
old-project: medfound
ms.assetid: 98052f26-7956-4973-ab86-428e7a355937
ms.author: windowssdkdev
ms.date: 07/18/2018
ms.keywords: ITocEntryList, ITocEntryList interface [Media Foundation], ITocEntryList interface [Media Foundation],described, codecapi.itocentrylist, mf.itocentrylist, wmcodecdsp/ITocEntryList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wmcodecdsp.h
req.include-header: 
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
req.typenames: MFVideoDSPMode
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - ITocEntryList
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ITocEntryList interface


## -description


The <b>ITocEntryList</b> interface represents a list of entries in a table of contents. It provides methods for adding entries to, and removing entries from the list.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ITocEntryList</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ITocEntryList</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ITocEntryList</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4ac41f10-4bb5-4d50-9f7b-7c8710476162">AddEntry</a>
</td>
<td align="left" width="63%">
Adds an individual entry to the list and assigns an index to the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c8146c0f-ac91-42c7-9368-dd2db6079d3d">AddEntryByIndex</a>
</td>
<td align="left" width="63%">
Adds an individual entry to the list and associates a caller-supplied index with the entry.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cf2171c9-67ce-4acb-97cc-af17203e815b">GetEntryByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an entry, specified by an index, from the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/74c45032-578d-4ee1-a13d-f95646f27ce9">GetEntryCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entries in the list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/72b9141c-2e61-42be-a4a1-910b607ab5f1">RemoveEntryByIndex</a>
</td>
<td align="left" width="63%">
Removes an entry, specified by an index, from the list.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/25039e6c-dd2a-4516-bf27-8e9d6ca0f00e">Table of Contents Parser Interfaces</a>
 

 

