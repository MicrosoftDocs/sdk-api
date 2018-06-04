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

# IWMIndexer interface


## -description



The <b>IWMIndexer</b> interface is used to create an index for ASF files to enable seeking. An index is created only for a file that contains video, although the indexer can safely be used on files that do not contain any video.

An index is an object in the ASF file that equates video samples with presentation times. This is important because the timing of video frames is not necessarily easily computed from the <a href="wmformat_glossary.htm">frame rate</a>.

In addition to the standard temporal index, the indexer object can create indexes based on video frame number and SMPTE time code. For more information about creating these indexes, see <a href="https://msdn.microsoft.com/b4ab9ad8-5fc7-43ce-ba2f-f32135a44a86">IWMIndexer2::Configure</a>.

This interface can be obtained by using the <a href="https://msdn.microsoft.com/08f83923-ed33-41d2-b7f8-d70627197b31">WMCreateIndexer</a> function.




## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IWMIndexer</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IWMIndexer</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IWMIndexer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh406716">Cancel</a>
</td>
<td align="left" width="63%">
Cancels indexing.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/67dfb0df-4883-49e1-a085-0b78db3967d0">StartIndexing</a>
</td>
<td align="left" width="63%">
Initiates indexing.

</td>
</tr>
</table> 

The following interface can be obtained by using the QueryInterface method of this interface.

<table>
<tr>
<th>Interface</th>
<th>IID</th>
</tr>
<tr>
<td>
<a href="https://msdn.microsoft.com/ce900a2b-765b-46bb-87f4-bf9fe57d1cdb">IWMIndexer2</a>
</td>
<td>IID_IWMIndexer2</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/652e04a5-ed6e-4e92-acf4-55ed82f77ef1">Indexer Object</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/dn965732">Interfaces</a>
 

 

