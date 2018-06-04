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

# IWMPContentPartner::GetListContents


## -description



<div class="alert"><b>Note</b>  This section describes functionality designed for use by online stores. Use of this functionality outside the context of an online store is not supported.</div>
<div> </div>
The <b>GetListContents</b> method initiates the retrieval of a dynamic list.




## -parameters




### -param location [in]

A library location constant that specifies the type of library view that will have its list retrieved. For example, the constant g_szCPListID specifies that a particular list will be retrieved.


### -param pContext [in]

The ID of the specific item that will have its list retrieved. For example, if <i>location</i> is g_szCPListID, then this parameter is the ID of the list that will be retrieved.


### -param bstrListType [in]

A library location constant that specifies the type of an individual list item. For example, the constant g_szCPAlbumID specifies that the items in the list are albums.


### -param bstrParams [in]

Parameters, meaningful only to the online store, associated with the retrieved list. See Remarks.


### -param dwListCookie [in]

A cookie used to identify the list retrieval operation. (The plug-in passes this cookie to <a href="https://msdn.microsoft.com/22d28495-310e-4f3d-a0e3-8f6679c78c40">IWMPContentPartnerCallback::AddListContents</a> and <a href="https://msdn.microsoft.com/e46a3378-a8e3-40c1-9cca-b6444286b3b5">IWMPContentPartnerCallback::ListContentsComplete</a>.)


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



Retrieving list contents is an asynchronous operation. This method should initiate the retrieval and return immediately. Then the plug-in must make one or more calls to <a href="https://msdn.microsoft.com/22d28495-310e-4f3d-a0e3-8f6679c78c40">IWMPContentPartnerCallback::AddListContents</a> to supply Windows Media Player with the requested list contents. When the plug-in has supplied all the data, it must call <a href="https://msdn.microsoft.com/e46a3378-a8e3-40c1-9cca-b6444286b3b5">IWMPContentPartnerCallback::ListContentsComplete</a> to signal the end of the operation. In each case, the plug-in passes the cookie provided in <i>dwListCookie</i> to identify the correct list retrieval session.




## -see-also




<a href="https://msdn.microsoft.com/2078ebd4-3570-4c39-9081-1b55d9e8286f">IWMPContentPartner Interface</a>
 

 

