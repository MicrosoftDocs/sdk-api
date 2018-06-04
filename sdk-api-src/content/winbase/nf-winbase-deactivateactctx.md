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

# DeactivateActCtx function


## -description


The 
<b>DeactivateActCtx</b> function deactivates the activation context corresponding to the specified cookie.


## -parameters




### -param dwFlags [in]

Flags that indicate how the deactivation is to occur. 



<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="0"></a><dl>
<dt><b>0</b></dt>
</dl>
</td>
<td width="60%">
If this value is set and the cookie specified in the <i>ulCookie</i> parameter is in the top frame of the activation stack, the activation context is popped from the stack and thereby deactivated. 




If this value is set and the cookie specified in the <i>ulCookie</i> parameter is not in the top frame of the activation stack, this function  searches down the stack for the cookie.

If the cookie is found, a STATUS_SXS_EARLY_DEACTIVATION exception is thrown.

If the cookie is not found, a STATUS_SXS_INVALID_DEACTIVATION exception is thrown.

This value should be specified in most cases.

</td>
</tr>
<tr>
<td width="40%"><a id="DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION"></a><a id="deactivate_actctx_flag_force_early_deactivation"></a><dl>
<dt><b>DEACTIVATE_ACTCTX_FLAG_FORCE_EARLY_DEACTIVATION</b></dt>
</dl>
</td>
<td width="60%">
If this value is set and the cookie specified in the <i>ulCookie</i> parameter is in the top frame of the activation stack, the function  returns an ERROR_INVALID_PARAMETER error code. Call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a> to obtain this code. 




If this value is set and the cookie is not on the activation stack, a STATUS_SXS_INVALID_DEACTIVATION exception will be thrown.

If this value is set and the cookie is in a lower frame of the activation stack, all of the frames down to and including the frame the cookie is in is popped from the stack.

</td>
</tr>
</table>
 


### -param ulCookie [in]

The ULONG_PTR that was passed into the call to 
<a href="https://msdn.microsoft.com/03381d95-1b5d-4b70-8c86-937ab9b2672d">ActivateActCtx</a>. This value is used as a cookie to identify a specific activated activation context.


## -returns



If the function succeeds, it returns <b>TRUE</b>. Otherwise, it returns <b>FALSE</b>.

This function sets errors that can be retrieved by calling 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. For an example, see 
<a href="https://msdn.microsoft.com/4cc626ac-7574-44ce-8377-e0bdd8e74b7e">Retrieving the Last-Error Code</a>. For a complete list of error codes, see 
<a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>.




## -remarks



The deactivation of activation contexts must occur in the reverse order of activation. It can be understood as popping an activation context from a stack.




## -see-also




<a href="https://msdn.microsoft.com/03381d95-1b5d-4b70-8c86-937ab9b2672d">ActivateActCtx</a>
 

 

