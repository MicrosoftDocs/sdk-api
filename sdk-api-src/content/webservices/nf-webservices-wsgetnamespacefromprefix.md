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

# WsGetNamespaceFromPrefix function


## -description


This function returns a namespace from the prefix to which it is bound.
      


        If the value of the <i>required</i> parameter is set to <b>TRUE</b> and the Prefix is not bound to any namespace a <b>WS_E_INVALID_FORMAT</b> exception will be returned.
        (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) If the <i>required</i> parameter is  <b>FALSE</b>, and the Prefix is not bound to any namespace the <i>ns</i> parameter will be <b>NULL</b> and the function will return S_FALSE.
      


## -parameters




### -param reader [in]


          A pointer to the reader for which the prefix should be searched.  


### -param prefix [in]

A pointer to the Prefix to search for.
        


### -param required [in]

The value of this Boolean parameter determines
          whether or not an error should be returned if a matching namespace is not found.
        


### -param ns

A reference to a namespace to which the prefix is bound if successful.  The value returned is valid only until the writer advances.
        


### -param error [in, optional]

A  pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object where additional information about the error should be stored if the function fails.
                


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




        For the prefix "xml" it will return the namespace "http://www.w3.org/XML/1998/namespace".
      


        For the prefix "xmlns" it will return the namespace "http://www.w3.org/2000/xmlns/".
      



