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

# tagFUNCDESC structure


## -description


Describes a function.


## -struct-fields




### -field memid

The function member ID.


### -field lprgscode

The status code.


### -field lprgelemdescParam

Description of the element.


### -field funckind

Indicates the type of function (virtual, static, or dispatch-only).


### -field invkind

The invocation type. Indicates whether this is a property function, and if so, which type.


### -field callconv

The calling convention.


### -field cParams

The total number of parameters.


### -field cParamsOpt

The number of optional parameters.


### -field oVft

For FUNC_VIRTUAL, specifies the offset in the VTBL.


### -field cScodes

The number of possible return values.


### -field elemdescFunc

The function return type.


### -field wFuncFlags

The function flags. See <a href="https://msdn.microsoft.com/290f8769-dde4-47b9-b3bb-680efc95f532">FUNCFLAGS</a>.


## -remarks



The <b>cParams</b> field specifies the total number of required and optional parameters.



The <b>cParamsOpt</b> field specifies the form of optional parameters accepted by the function, as follows:

<ul>
<li>
A value of 0 specifies that no optional arguments are supported.



</li>
<li>
A value of –1 specifies that the method's last parameter is a pointer to a safe array of variants. Any number of variant arguments greater than <b>cParams</b> –1 must be packaged by the caller into a safe array and passed as the final parameter. This array of optional parameters must be freed by the caller after control is returned from the call.



</li>
<li>
Any other number indicates that the last n parameters of the function are variants and do not need to be specified by the caller explicitly. The parameters left unspecified should be filled in by the compiler or interpreter as variants of type VT_ERROR with the value DISP_E_PARAMNOTFOUND.



</li>
</ul>


