---
UID: NN:imapi2fs.IEnumFsiItems
title: IEnumFsiItems
author: windows-sdk-content
description: Use this interface to enumerate the child directory and file items for a FsiDirectoryItem object.
old-location: imapi\ienumfsiitems.htm
tech.root: imapi
ms.assetid: f3186af1-4056-4cb5-aac4-5253ee6dbc01
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumFsiItems, IEnumFsiItems interface [IMAPI], IEnumFsiItems interface [IMAPI],described, imapi.ienumfsiitems, imapi2fs/IEnumFsiItems
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: imapi2fs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista, Windows XP with SP2 [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Imapi2fs.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - imapi2fs.h
api_name:
 - IEnumFsiItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumFsiItems interface


## -description


Use this interface to enumerate the child directory and file items for a FsiDirectoryItem object.

To get this interface, call the <a href="https://msdn.microsoft.com/723f28ad-f77d-494f-9ae6-ba6120675cfd">IFsiDirectoryItem::get_EnumFsiItems</a> method.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IEnumFsiItems</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IEnumFsiItems</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IEnumFsiItems</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/70806e80-c6b3-4f9c-8146-7dde1c895812">Clone</a>
</td>
<td align="left" width="63%">
Creates another enumerator that contains the same enumeration state as the current one.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3aad9540-7fbc-4eda-9619-187a9c5b4b2d">Next</a>
</td>
<td align="left" width="63%">
Retrieves a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/a5ae59ed-08d7-4225-9aec-91049789e8fe">RemoteNext</a>
</td>
<td align="left" width="63%">
Supports a remote client that wants to retrieve a specified number of items in the enumeration sequence.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/85b3ce47-411f-4824-acea-9ea974206672">Reset</a>
</td>
<td align="left" width="63%">
Resets the enumeration sequence to the beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f1bf8542-12b9-4228-9e0e-1defbb57cac3">Skip</a>
</td>
<td align="left" width="63%">
Skips a specified number of items in the enumeration sequence.

</td>
</tr>
</table> 


## -remarks



This is a <b>EnumFsiItems</b> object in script.




## -see-also




<a href="https://msdn.microsoft.com/0256f1d2-a3fb-45b2-bd84-e2b71148e4ec">IFileSystemImage</a>



<a href="https://msdn.microsoft.com/1c9a2e36-0e79-4bad-b880-ddfbf473308b">IFsiDirectoryItem</a>
 

 

