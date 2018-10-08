---
UID: NN:wmcodecdsp.IToc
title: IToc
author: windows-sdk-content
description: The IToc interface represents an individual table of contents. It provides methods for adding entries to, and removing entries from the table of contents.
old-location: mf\itoc.htm
tech.root: medfound
ms.assetid: b12d38c7-b80e-4ca8-9ac5-a116100911d0
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: IToc, IToc interface [Media Foundation], IToc interface [Media Foundation],described, codecapi.itoc, mf.itoc, wmcodecdsp/IToc
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
req.lib: 
req.dll: Wmvdspa.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmvdspa.dll
api_name:
 - IToc
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IToc interface


## -description


The <b>IToc</b> interface represents an individual table of contents. It provides methods for adding  entries to, and removing entries from the table of contents.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IToc</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IToc</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IToc</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8d04d6b8-d110-45a3-b3bb-5a7b680ddabe">AddEntryList</a>
</td>
<td align="left" width="63%">
Adds an entry list to the table of contents and assigns an index to the entry list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/273e1c38-7f1a-4f04-b1a8-ba27b5babf94">AddEntryListByIndex</a>
</td>
<td align="left" width="63%">
Adds an entry list to the table of contents and associates a caller-supplied index with the entry list.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/b4c65f1b-7465-4229-8fac-92d6b1be50da">GetContext</a>
</td>
<td align="left" width="63%">
Retrieves a block of bytes that was previously associated with the table of contents by a call to <a href="https://msdn.microsoft.com/45aadac5-6c65-4525-a1fc-b045337a6030">SetContext</a>.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/660d4da9-ddbc-466c-ab1a-7e60ecf61473">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves the description, set by a previous call to <a href="https://msdn.microsoft.com/718eb8bd-fdf9-434d-b859-3a38cb8fabee">SetDescription</a>, of the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/4568b50f-a777-4c3d-8c71-66737d24b7cd">GetDescriptor</a>
</td>
<td align="left" width="63%">
Retrieves the descriptor, previously set by <a href="https://msdn.microsoft.com/55208226-fd2d-48e5-887b-34e95309a770">SetDescriptor</a>, of the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/5c457eb4-3034-40e3-93b6-e421c2e34bcf">GetEntryListByIndex</a>
</td>
<td align="left" width="63%">
Retrieves an entry list, specified by an index, from the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/38348080-e188-4d58-8d46-dc954da398e6">GetEntryListCount</a>
</td>
<td align="left" width="63%">
Retrieves the number of entry lists in the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/63137b67-dc00-48e7-88b0-2f7159c1d829">RemoveEntryListByIndex</a>
</td>
<td align="left" width="63%">
Removes an entry list, specified by an index, from the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/45aadac5-6c65-4525-a1fc-b045337a6030">SetContext</a>
</td>
<td align="left" width="63%">
Associates a caller-supplied context block with the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/718eb8bd-fdf9-434d-b859-3a38cb8fabee">SetDescription</a>
</td>
<td align="left" width="63%">
Associates a description with the table of contents.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/55208226-fd2d-48e5-887b-34e95309a770">SetDescriptor</a>
</td>
<td align="left" width="63%">
Associates a descriptor with the table of contents.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>



<a href="https://msdn.microsoft.com/25039e6c-dd2a-4516-bf27-8e9d6ca0f00e">Table of Contents Parser Interfaces</a>
 

 

