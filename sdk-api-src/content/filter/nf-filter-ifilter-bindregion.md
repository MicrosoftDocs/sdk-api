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

# IFilter::BindRegion


## -description


<p class="CCE_Message">[Indexing Service is no longer supported as of Windows XP and is unavailable for use as of Windows 8. Instead, use <a href="https://msdn.microsoft.com/6da601c6-3742-40ad-99f2-8817f7f642b3">Windows Search</a> for client side search and  <a href=" http://go.microsoft.com/fwlink/p/?linkid=258445">Microsoft Search Server Express</a> for server side search.]

Retrieves an interface representing the specified portion of object. Currently reserved for future use.


## -parameters




### -param origPos [in]

A <a href="https://msdn.microsoft.com/cb2ea1d4-ee94-4626-bdd0-c822ad068e90">FILTERREGION</a> structure that contains the position of the text. 



### -param riid [in]

A reference to the requested interface identifier.


### -param ppunk [out]

A pointer to a variable that receives the interface pointer requested in <i>riid</i>. Upon successful return, *<i>ppunk</i> contains the requested interface pointer.


## -returns



This method can return one of these values.

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
The operation was completed successfully.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
This method is not currently implemented.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>FILTER_W_REGION_CLIPPED</b></dt>
</dl>
</td>
<td width="60%">
The filter could not bind the entire region.

</td>
</tr>
</table>
 




## -remarks



If it is impossible for the <b>BindRegion</b> method to bind an interface to the specified region, return FILTER_W_REGION_CLIPPED. This situation can occur when the next such chunk is in a linked object or an embedded object. 



Not all filters are capable of supporting the <b>BindRegion</b> method in a rational way. Filters that are implemented by viewing applications will benefit the most from this method. The method is intended to be a way to pass cookies through the search engine and back to the <a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a> interface implementation. 

<h3><a id="Notes_to_Implementers"></a><a id="notes_to_implementers"></a><a id="NOTES_TO_IMPLEMENTERS"></a>Notes to Implementers</h3>
This method is currently reserved for future use. Always return E_NOTIMPL.






## -see-also




<a href="https://msdn.microsoft.com/5fb7219a-608c-43f8-a8e3-48bbf0218c6e">IFilter</a>
 

 

