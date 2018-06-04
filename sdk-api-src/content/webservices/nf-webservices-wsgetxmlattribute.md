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

# WsGetXmlAttribute function


## -description



        Finds the nearest xml attribute in scope with the specified localName and returns its value.  
        The returned value is placed on the specified heap.
      


## -parameters




### -param reader [in]


          The reader for which the xml attribute will be searched.
        


### -param localName [in]


          The localName of the xml attribute for which to search.
        


### -param heap [in]


          The heap on which the resulting value should be allocated.
        


### -param valueChars


          The value of the attribute is stored here.
        


### -param valueCharCount [out]


          The length of the valueChars.
        


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

One or more arguments are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">


        The xml attribute was not found.
      

</td>
</tr>
</table>
 




## -remarks




        This function may only be used to obtain the values of attributes in scope that use the prefix "xml".
      


        If no matching xml attribute is found, a zero length string will be returned for the value, and the
        function returns S_FALSE.
      


        The reader does not do anything with xml attributes other than to surface them for inspection.
      



