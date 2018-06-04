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

# IWMPPlaylist::get_attributeName


## -description



The <b>get_attributeName</b> method retrieves the name of an attribute specified by an index.




## -parameters




### -param lIndex [in]

<b>long</b> containing the index.


### -param pbstrAttributeName [out]

Pointer to a <b>BSTR</b> containing the attribute name.


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



The number of attributes is retrieved by the <b>get_attributeCount</b> method.

The <i>pbstAttributeName</i> string can be supplied to the <b>setItemInfo</b> or <b>getItemInfo</b> methods to specify or retrieve a value for the named attribute.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

For information about the attributes supported by Windows Media Player, see the Windows Media Player <a href="https://msdn.microsoft.com/a333ee0d-8f74-4517-b4c7-b1d8f95df2fc">Attribute Reference</a>.




## -see-also




<a href="https://msdn.microsoft.com/04b6d6bc-a3fe-4b3f-b348-0f6b9f6e77a9">IWMPPlaylist Interface</a>



<a href="https://msdn.microsoft.com/c6763274-01e4-4a2f-9467-150e1964193a">IWMPPlaylist::getItemInfo</a>



<a href="https://msdn.microsoft.com/32c18feb-4df2-41d6-9adf-49836b6b836d">IWMPPlaylist::get_attributeCount</a>



<a href="https://msdn.microsoft.com/fd812af6-0bdf-4da4-a066-4411d0d9e259">IWMPPlaylist::setItemInfo</a>
 

 

