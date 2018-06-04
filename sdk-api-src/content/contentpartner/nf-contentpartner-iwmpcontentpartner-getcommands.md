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

# IWMPContentPartner::GetCommands


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetCommands</b> method retrieves context menu commands.




## -parameters




### -param location [in]

A <a href="https://msdn.microsoft.com/88ff9b91-6b21-4f7d-ae13-e8456a3e0f75">library location constant</a> that specifies the type of library view where the user right-clicked. For example, the constant g_szCPGenreID indicates that the user right-clicked in the view of a particular genre


### -param pLocationContext [in]

The ID of the specific view where the user right-clicked. For example, if <i>location</i> is g_szCPGenreID, this parameter is the ID of the particular genre the user was viewing when he or she right-clicked.


### -param itemLocation [in]

A library location constant that indicates the type of the media item or items that were selected when the user right-clicked. For example, the constant g_szCPAlbumID specifies that the user right-clicked when one or more albums were selected.


### -param cItemIDs [in]

The number of items that were selected when the user right-clicked. This is the number of elements in the prgIte<i></i>mIDs array.


### -param prgItemIDs [in]

An array that contains the IDs of the media items that were selected when the user right-clicked.


### -param pcItemIDs [out]

The number of elements in the <i>pprgItems</i> array.


### -param pprgItems [out]

Address of a variable that receives a pointer to an array of <a href="https://msdn.microsoft.com/a37ddbe1-7c66-4060-b93d-bd494cdc4521">WMPContextMenuInfo</a> structures.


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



This method must call <b>CoTaskMemAlloc</b> to allocate the array that it returns in <i>pprgItems</i>.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>
 

 

