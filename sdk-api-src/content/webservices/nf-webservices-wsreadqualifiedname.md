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

# WsReadQualifiedName function


## -description



        Reads a qualified name and separates it into its prefix, localName 
        and namespace based on the current namespace scope of the XML_READER. 
        If the ns parameter is specified, then the namespace that the prefix 
        is bound to will be returned, or <b>WS_E_INVALID_FORMAT</b>
        will be returned. (See <a href="https://msdn.microsoft.com/96285557-8317-4875-b634-e2eacd605901">Windows Web Services Return Values</a>.) The strings are placed in the specified heap.
      


## -parameters




### -param reader [in]


          The reader which should read the qualified name.
        


### -param heap [in]


          The heap on which the resulting strings should be allocated.
        


### -param prefix


          The prefix of the qualified name is returned here.
        


### -param localName [out]


          The localName of the qualified name is returned here.
        


### -param ns


          The namespace to which the qualified name is bound is returned here.
        


### -param error [in, optional]


          If the localName is missing the function will return <b>WS_E_INVALID_FORMAT</b>.  
          If the ns parameter is specified, but the prefix is not bound to a namespace, 
           <b>WS_E_INVALID_FORMAT</b> will be returned.
        


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
 



