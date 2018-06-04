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

# WsAddCustomHeader function


## -description




                Adds the specified application-defined header to the <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a>.
            




## -parameters




### -param message [in]


                    The message to which to add the header.
                


                    The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b> (see the <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE</a> enumeration..
                


### -param headerDescription [in]


                    The <a href="https://msdn.microsoft.com/17035b64-9b2c-40d3-bdce-45e9b132e9f1">WS_ELEMENT_DESCRIPTION</a> structure that describes the header.
                


### -param writeOption [in]


                    Whether the header element is required, and how the value is allocated.
                    For more information, see the <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> enumeration.
                


### -param value [in, ref]


                    The header value to serialize.  For more information, see  the <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> enumeration.
                
                


### -param valueSize [in]


                    The size of the value being serialized, in bytes.
                


### -param headerAttributes [in]

The values of the SOAP attributes for the header.
                


### -param error [in, optional]


                    Pointer to a <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure  that receives additional error information if the function fails.
                


## -returns



If the function succeeds, it returns NO_ERROR; otherwise, it returns an HRESULT error code.

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

                    There are multiple instances of the same type of header present in the message.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory to complete the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">

                    One or more of the parameters are incorrect.
                

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




                The <b>WsAddCustomHeader</b> function is designed handle types of headers that are targeted at 
                the final receiver.  Headers targeted at another receiver are ignored.
            


                If you are replacing a header, call the <a href="https://msdn.microsoft.com/def38214-2de9-4a26-93cb-e2f34d8dd6ef">WsRemoveCustomHeader</a> function to remove 
                the existing instances of the header before calling <b>WsAddCustomHeader</b>.
            



