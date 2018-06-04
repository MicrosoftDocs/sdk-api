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

# tagProxyFileInfo structure


## -description


The <b>ProxyFileInfo</b> structure contains information about the interface proxies in the proxy DLL.


## -struct-fields




### -field pProxyVtblList

Array of proxy Vtables contained in the proxy DLL. Each array element contains the Vtable for each proxy interface in the DLL.


### -field pStubVtblList

 


### -field pNamesArray

Array of interface names contained in the proxy DLL. 


### -field pDelegatedIIDs

Array of base interface identifiers contained in the proxy DLL. Array elements associated with interfaces that are not delegated are set to null. If no interfaces in the DLL are delegated, <i>pDelegatedIIDs</i> is null. 


### -field pIIDLookupRtn

Used to search for a given interface in the proxy list.


### -field TableSize

Number of interfaces in the proxy DLL.


### -field TableVersion

Version of the proxy stub. The version can be one of the versions.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The .idl file is compiled with the <a href="https://msdn.microsoft.com/dc5cafbb-dcc6-4fcb-a04f-1bc9720a13cb">/0s</a> option. 

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The .idl file is compiled with the <a href="midl._oi">/0i</a>, <b>/0ic</b>, or <b>/Oicf</b> option.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt>6</dt>
</dl>
</td>
<td width="60%">
The proxy DLL contains an asynchronous interface.

</td>
</tr>
</table>
 


### -field pAsyncIIDLookup

Used to search for a given asynchronous interface in the proxy list.


### -field Filler2

Not used.


### -field Filler3

Not used.


### -field Filler4

Not used.


#### - pstubVtblList

Array of stub Vtables contained in the proxy DLL. Each array element contains the Vtable for each stub interface in the DLL.

