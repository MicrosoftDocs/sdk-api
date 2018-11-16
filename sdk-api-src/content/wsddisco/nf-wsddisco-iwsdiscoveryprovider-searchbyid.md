---
UID: NF:wsddisco.IWSDiscoveryProvider.SearchById
title: IWSDiscoveryProvider::SearchById
author: windows-sdk-content
description: Initializes a search for WS-Discovery hosts by device identifier.
old-location: ncd\iwsdiscoveryprovider_searchbyid.htm
tech.root: WsdApi
ms.assetid: 78ae714a-1ee3-46eb-b3d6-ff46bf8974ab
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWSDiscoveryProvider interface,SearchById method, IWSDiscoveryProvider.SearchById, IWSDiscoveryProvider::SearchById, SearchById, SearchById method, SearchById method,IWSDiscoveryProvider interface, ncd.iwsdiscoveryprovider_searchbyid, wsddisco/IWSDiscoveryProvider::SearchById
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wsddisco.h
req.include-header: Wsdapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wsddisco.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Wsdapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wsdapi.dll
api_name:
 - IWSDiscoveryProvider.SearchById
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wsddisco.h
: 
- IWSDiscoveryProvider.SearchById
: 
---

# IWSDiscoveryProvider::SearchById


## -description


Initializes a search for <a href="http://go.microsoft.com/fwlink/p/?linkid=87841">WS-Discovery</a> hosts by device identifier.


## -parameters




### -param pszId [in]

Device identifier of the desired discovery provider.


### -param pszTag [in, optional]

Optional identifier tag for this search.  May be <b>NULL</b>.


## -returns



Possible return values include, but are not limited to, the following:

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
Method completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pszId</i> is <b>NULL</b>, the length in characters of <i>pszId</i>  exceeds WSD_MAX_TEXT_LENGTH (8192), or the length in characters of  <i>pszTag</i> exceeds WSD_MAX_TEXT_LENGTH (8192).

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ABORT</b></dt>
</dl>
</td>
<td width="60%">
A callback interface has not been attached. You must call <a href="https://msdn.microsoft.com/3bb2aead-b082-4a2b-b4bf-97a1feb1e11e">Attach</a> before calling this method.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Not enough memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



<b>SearchById</b> initiates a WS-Discovery <a href="https://msdn.microsoft.com/b963bd2a-47cb-4f8d-8272-a586e6d6a047">Resolve</a> in an attempt to locate a previously known specific device. <i>pszId</i> is used as the endpoint address in the Resolve. This call may result in one or more <a href="https://msdn.microsoft.com/4e36157f-444d-4e59-bc30-c6def9c51cea">Add</a> callbacks. If any <b>Add</b> callbacks are issued before the search completes, a <a href="https://msdn.microsoft.com/a125a7b3-6887-42e2-b421-d0e27973d8ee">SearchComplete</a> callback will be issued; otherwise, a <a href="https://msdn.microsoft.com/8f861c69-2967-4a8d-a64a-e2409d722984">SearchFailed</a> callback will be issued.

<i>pszTag</i> is an optional user provided string which will be fed back in either callback, allowing the caller to associate the callback with the original query.

For information about troubleshooting applications calling this method, see <a href="https://msdn.microsoft.com/befe4234-8d3a-4fc5-9a7d-faca94964af6">Troubleshooting WSDAPI Applications</a>.




## -see-also




<a href="https://msdn.microsoft.com/e3d3acc2-914b-40bd-9e1e-a3a612821ab7">IWSDiscoveryProvider</a>
 

 

