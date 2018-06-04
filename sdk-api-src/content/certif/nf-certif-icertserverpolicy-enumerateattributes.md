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

# ICertServerPolicy::EnumerateAttributes


## -description


The <b>EnumerateAttributes</b> method retrieves the name of the current attribute and moves the internal enumeration pointer to the next  attribute.


## -parameters




### -param pstrAttributeName [out]

A pointer to the attribute name.


## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK, and the <i>pstrAttributeName</i> parameter is set to a <b>BSTR</b> that contains the name of the  attribute. A value of S_FALSE is returned if the last attribute was already enumerated.

To use this method, create a variable of <b>BSTR</b> type, set the variable equal to <b>NULL</b>, and then pass the address of this variable as <i>pstrAttributeName</i>.

When you have finished using the <b>BSTR</b>, free it by calling the <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> function.

If the method fails, it returns an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.

<h3>VB</h3>
 Returns a string that contains the name of the attribute, or an empty string if the last attribute was already enumerated.




## -remarks



Before calling the <b>EnumerateAttributes</b>  method for the first time, call 
the <a href="https://msdn.microsoft.com/14b81b88-36db-4b01-96e6-eafed22ae02e">EnumerateAttributesSetup</a> method to initialize the enumeration pointer to the first attribute.

 When done enumerating, call  
the <a href="https://msdn.microsoft.com/91cb8edd-7735-44c5-b2c5-d46fa1e33e41">EnumerateAttributesClose</a> method to free resources used by the enumeration calls.




## -see-also




<a href="https://msdn.microsoft.com/7d16161e-9827-46a0-9989-30ebca792bb1">ICertServerPolicy</a>



<a href="https://msdn.microsoft.com/91cb8edd-7735-44c5-b2c5-d46fa1e33e41">ICertServerPolicy::EnumerateAttributesClose</a>



<a href="https://msdn.microsoft.com/14b81b88-36db-4b01-96e6-eafed22ae02e">ICertServerPolicy::EnumerateAttributesSetup</a>
 

 

