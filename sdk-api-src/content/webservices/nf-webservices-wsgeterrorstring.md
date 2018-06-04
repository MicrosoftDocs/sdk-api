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

# WsGetErrorString function


## -description



                Retrieves an error string from an error object.
            


## -parameters




### -param error [in]


                    The error object containing the string.
                


### -param index [in]


                    The zero-based index identifying the string to retrieve.  The first
                    error string (index 0) will be the string most recently added to the
                    error object (using <a href="https://msdn.microsoft.com/5fdad296-5024-4360-b1c5-f0192929c612">WsAddErrorString</a>). When 
                    <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_ORIGINAL_ERROR_CODE</a> is presented in the 
                    error object, the corresponding error text will be available in the last index.
                


                    The number of errors can be retrieved using <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_STRING_COUNT</a>.
                


### -param string [out]


                    The returned string.  The string is valid until <a href="https://msdn.microsoft.com/a01a65f1-3eca-452c-a10d-dc9c6c3db124">WsResetError</a>
                    or <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> is called.
                


                    The string is not zero terminated.
                


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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 




## -remarks




                The string is in the language specified by the LANGID property of
                the error object.  This can be retrieved using <a href="https://msdn.microsoft.com/35a1f4a8-aad6-43ad-81db-b1071a77d5f4">WsGetErrorProperty</a>
                with <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_LANGID</a>.
            



