---
UID: NN:cscobj.IEnumOfflineFilesItems
title: IEnumOfflineFilesItems
author: windows-sdk-content
description: Represents a collection of IOfflineFilesItem interface pointers.
old-location: of\ienumofflinefilesitems.htm
tech.root: offlinefiles
ms.assetid: 9bb1fa14-74d2-4c6f-b8ba-47c6e78d7a4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IEnumOfflineFilesItems, IEnumOfflineFilesItems interface [Offline Files], IEnumOfflineFilesItems interface [Offline Files],described, cscobj/IEnumOfflineFilesItems, of.ienumofflinefilesitems
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IEnumOfflineFilesItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumOfflineFilesItems interface


## -description


Represents a collection of <a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a> interface pointers.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumOfflineFilesItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumOfflineFilesItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumOfflineFilesItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cef0adaf-d342-4eab-b455-2b51b7d70066">Clone</a>
</td>
<td align="left" width="63%">
Creates a new instance of the enumerator with the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/509bb93a-0ab4-4e4a-935a-c30e6b1f03fd">Next</a>
</td>
<td align="left" width="63%">
Retrieves the next item in the enumeration and advances the enumerator.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/fa4d1313-e05d-49be-80c3-cbb70463dfb1">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/e1f201c4-6ca8-49ca-af05-003a09ec86bd">Skip</a>
</td>
<td align="left" width="63%">
Skips over the next specified number of elements in the enumeration.

</td>
</tr>
</table> 


## -remarks



To obtain an instance of this interface, first obtain an instance of <a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a> using <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> on an instance of one of the following interfaces:

<ul>
<li>
<a href="https://msdn.microsoft.com/7b1b5ef6-355a-4760-9d54-ec73cc66fb8a">IOfflineFilesCache</a>
</li>
<li>
<a href="https://msdn.microsoft.com/9300b4f3-1261-40d2-ae05-fb1be2f857b9">IOfflineFilesDirectoryItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/724fabf6-fb27-49c9-8f99-dc61377ac921">IOfflineFilesServerItem</a>
</li>
<li>
<a href="https://msdn.microsoft.com/aff6be4a-07bc-4a74-8fbf-92fe8985f5b6">IOfflineFilesShareItem</a>
</li>
</ul>
<div class="alert"><b>Note</b>  The <a href="https://msdn.microsoft.com/328ad076-cafd-461e-8085-7fca65063fa0">IOfflineFilesItemContainer</a> interface is only valid for directory, server, and share items. If <a href="https://msdn.microsoft.com/en-us/library/ms682521(v=VS.85).aspx">QueryInterface</a> is called for the <b>IOfflineFilesItemContainer</b> interface on a file item (an instance of the <a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a> interface), it will fail with <b>E_NOINTERFACE</b>.</div>
<div> </div>
For a code example that shows how to use the <b>IEnumOfflineFilesItems</b> interface, see <a href="https://msdn.microsoft.com/9960e8f8-4d15-4a53-aa77-d0105b6a59d1">IOfflineFilesItemContainer::EnumItems</a>.




## -see-also




<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

