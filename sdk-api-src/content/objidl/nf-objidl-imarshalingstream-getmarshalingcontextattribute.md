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

# IMarshalingStream::GetMarshalingContextAttribute


## -description


Gets information about the marshaling context.


## -parameters




### -param attribute [in]

The attribute to query.


### -param pAttributeValue [out]


            The value of <i>attribute</i>.
          


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Each possible value of the attribute parameter is paired with the data type of the attribute this identifies.

You can query the following attributes with this method.

<table>
<tr>
<th>Attribute</th>
<th>Values</th>
</tr>
<tr>
<td>
CO_MARSHALING_SOURCE_IS_APP_CONTAINER

</td>
<td>

                This attribute is a boolean value, with 0 representing <b>TRUE</b> and nonzero representing <b>FALSE</b>. You can safely cast the value of the result to <b>BOOL</b>, but it isn't safe for the caller to cast a <b>BOOL*</b> to <b>ULONG_PTR*</b> for the <i>pAttributeValue</i> parameter, or for the implementation to cast <i>pAttributeValue</i> to <b>BOOL*</b> when setting it.
              

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/EF020513-8E03-474C-BC14-9E9D6EFE7318">CO_MARSHALING_CONTEXT_ATTRIBUTES</a>



<a href="https://msdn.microsoft.com/c5e823be-521d-4eb4-8836-fdd2cac6f15d">IGlobalOptions</a>



<a href="https://msdn.microsoft.com/7C4A3982-3623-4F1F-929C-6D0503700450">IMarshalingStream</a>
 

 

