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

# WsFindAttribute function


## -description



        Searches the attributes of the current element for an attribute with the 
        specified name and namespace and returns its index which may be passed 
        to <a href="https://msdn.microsoft.com/6fd0c8c2-2eac-4d98-898d-1c5849220c36">WsReadStartAttribute</a>.
      


## -parameters




### -param reader [in]


          The reader on which to find the attribute.
        


### -param localName [in]


          The local name of the attribute to search for.
        


### -param ns [in]


          The namespace of the attribute to search for.
        


### -param required [in]


          If required is <b>TRUE</b> and the attribute is not found,  the function will return <b>WS_E_INVALID_FORMAT</b>.
          (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) if required is <b>FALSE</b> and the attribute is not found, the function will return S_FALSE.
        


### -param attributeIndex [out]


          If the attribute is found, then the index of the attribute, is returned here.
          This index can then be passed to <a href="https://msdn.microsoft.com/6fd0c8c2-2eac-4d98-898d-1c5849220c36">WsReadStartAttribute</a>.
        


### -param error [in, optional]


          Specifies where additional error information should be stored if the function fails.
        


## -returns



This function can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

</td>
</tr>
</table>
 




## -remarks




        If the reader is not positioned on a start element then it will return <b>WS_E_INVALID_OPERATION</b>.
      (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) 


        The index returned does not necessarily correspond to the position of the attribute as it appeared
        in the document.  It identifies the index of the matching attribute in the array of attributes of
        the <a href="https://msdn.microsoft.com/32157ddf-ace2-49dc-85d7-b04e25e85693">WS_XML_ELEMENT_NODE</a>.  The order of the attributes in this array may differ from the order
        in which the attributes appeared in the document.
      



