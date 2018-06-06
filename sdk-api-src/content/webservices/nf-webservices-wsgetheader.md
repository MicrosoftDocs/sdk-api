---
UID: NF:webservices.WsGetHeader
title: WsGetHeader function
author: windows-sdk-content
description: Finds a particular standard header in the message and deserializes it.
old-location: wsw\wsgetheader.htm
old-project: wsw
ms.assetid: ff6e639f-715d-4a4f-b0ef-35202aa54dc5
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsGetHeader, WsGetHeader function [Web Services for Windows], webservices/WsGetHeader, wsw.wsgetheader
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: WS_SECURITY_ALGORITHM_PROPERTY_ID
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetHeader
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsGetHeader function


## -description



                Finds a particular standard header in the message and deserializes it.
            


## -parameters




### -param message [in]


                    The message containing the header.
                


                    The message can be in any state but <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.
                


### -param headerType [in]


                    The type of header to deserialize.
                


### -param valueType [in]


                    The type of value to deserialize.  See <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a> for
                    the set of types which correspond to each type of header.
                


### -param readOption [in]


                    Whether the value is required, and how to allocate the value. 
                    <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_NILLABLE_VALUE</a> and <b>WS_READ_NILLABLE_POINTER</b> 
                    read options cannot be specified since the header types in <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a> 
                    are not allowed to be nillable in the respective standards specifications.
                    See <b>WS_READ_OPTION</b> for more information.
                


### -param heap [in, optional]


                    The heap to store the deserialized header data in.
                    If this is <b>NULL</b>, then the message heap will be used.
                


### -param value


                    The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a>.
                


### -param valueSize [in]


                    The interpretation of this parameter depends on the <a href="https://msdn.microsoft.com/634b057f-3121-43cc-919f-8636e67ce0d7">WS_READ_OPTION</a>.
                


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

                    The header does not exist, and is required.
                


                    There are multiple instances of the type of header present in the message.
                


                    The input data was not in the expected format.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

                    There size quota of the heap was exceeded.
                

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

                    There was not enough memory available to deserialize the header.
                

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




                This API provides access to a set of standard header types (see <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a>).
                For application defined header types, use <a href="https://msdn.microsoft.com/bdfb441b-afc4-4be8-b437-f299a31ce84b">WsGetCustomHeader</a>.
            


                This API is designed handle types of headers that appear once in the
                message and are targeted at the ultimate receiver.  Headers targeted
                with a role/actor other than ultimate receiver are ignored by this API.
            



