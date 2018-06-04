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

# IWMPContentPartner::InvokeCommand


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>InvokeCommand</b> method invokes a context menu command.




## -parameters




### -param dwCommandID [in]

ID of the command to invoke. Windows Media Player previously obtained this command ID from the content partner plug-in by calling <a href="https://msdn.microsoft.com/bc6dfd97-50bb-438c-9cd6-3eac91e99cab">IWMPContentPartner::GetCommands</a>.


### -param location [in]

A library location constant that specifies the type of library view where the user right-clicked. For example, the constant g_szCPGenreID specifies that the user right-clicked in the view of a particular genre.


### -param pLocationContext [in]

TheID of the specific view where the user right-clicked. For example, if <i>location</i> is g_szCPGenreID, then this parameter is the ID of the particular genre the user was viewing when he or she right-clicked.


### -param itemLocation [in]

A library location constant that specifies the type of the media item or items that were selected when the user right-clicked. For example, the constant g_szCPAlbumID specifies that the user right-clicked when one or more albums were selected.


### -param cItemIDs [in]

The number of items that were selected when the user right-clicked. This is the number of elements in the <i>rgItemIDs</i> array.


### -param rgItemIDs [in]

An array that contains the IDs of the media items that were selected when the user right-clicked.


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
 




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>
 

 

