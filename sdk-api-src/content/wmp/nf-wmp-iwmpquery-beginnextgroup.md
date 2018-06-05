---
UID: NF:wmp.IWMPQuery.beginNextGroup
title: IWMPQuery::beginNextGroup
author: windows-sdk-content
description: The beginNextGroup method begins a new condition group.
old-location: wmp\iwmpquery_beginnextgroup.htm
old-project: WMP
ms.assetid: c81a8125-2cfa-40e2-afc5-672c2866b880
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: IWMPQuery interface [Windows Media Player],beginNextGroup method, IWMPQuery.beginNextGroup, IWMPQuery::beginNextGroup, IWMPQuerybeginNextGroup, beginNextGroup, beginNextGroup method [Windows Media Player], beginNextGroup method [Windows Media Player],IWMPQuery interface, wmp.iwmpquery_beginnextgroup, wmp/IWMPQuery::beginNextGroup
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPQuery.beginNextGroup
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPQuery::beginNextGroup


## -description



The <b>beginNextGroup</b> method begins a new condition group.




## -parameters






## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



Beginning a new condition group implies that you have completed the current condition group. The new condition group is always concatenated to the previous condition group by using OR logic.

<b>Windows Media Player 10 Mobile: </b>This method is not supported.




## -see-also




<a href="https://msdn.microsoft.com/b1e6bf08-3b81-4c04-92ff-73eac5f7495a">IWMPMediaCollection2::createQuery</a>



<a href="https://msdn.microsoft.com/b3d4586b-c999-447c-b974-15bd0ef160a6">IWMPMediaCollection2::getPlaylistByQuery</a>



<a href="https://msdn.microsoft.com/070bc947-bf2b-4c06-9ffa-6a23625d178a">IWMPMediaCollection2::getStringCollectionByQuery</a>



<a href="https://msdn.microsoft.com/f1f3c46f-4756-49b4-ad4f-a9097ff787f8">IWMPQuery Interface</a>
 

 

