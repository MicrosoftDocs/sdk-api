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

# IShellDispatch5 interface


## -description


Extends the <a href="https://msdn.microsoft.com/4fe37e38-ee71-41f0-b620-35fdc18f9dbb">IShellDispatch4</a> object. In addition to the properties and methods supported by <b>IShellDispatch4</b>, <b>IShellDispatch5</b> adds a method that displays open windows in a 3D stack.

            
<div class="alert"><b>Note</b>  <b>IShellDispatch5</b> is implemented and accessed through the <a href="https://msdn.microsoft.com/library/windows/hardware/mt270130">Shell</a> object.</div><div> </div>

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IShellDispatch5</b> object has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IShellDispatch5</b> object has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/44a6411c-bcbc-4ef6-b5dc-7bdb4d482c6a">WindowSwitcher</a>
</td>
<td align="left" width="63%">
Displays your open windows in a 3D stack that you can flip through.

</td>
</tr>
</table> 


## -see-also




<a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a>



<a href="https://msdn.microsoft.com/9B429C03-7F80-45db-B8CD-58D19FAD2E61">IShellDispatch</a>



<a href="https://msdn.microsoft.com/74687929-0777-479b-9853-2b0cf4b6adc9">IShellDispatch2</a>



<a href="https://msdn.microsoft.com/89d0aa4d-844d-497d-82bb-bcc2bcf9c78b">IShellDispatch3</a>



<a href="https://msdn.microsoft.com/4fe37e38-ee71-41f0-b620-35fdc18f9dbb">IShellDispatch4</a>



<a href="https://msdn.microsoft.com/75fc151e-5b9e-476b-b4e5-b848917357a8">Shell Object</a>
 

 

