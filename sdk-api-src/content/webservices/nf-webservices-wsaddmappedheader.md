---
UID: NF:webservices.WsAddMappedHeader
title: WsAddMappedHeader function
author: windows-sdk-content
description: Adds a specified mapped header to the message.
old-location: wsw\wsaddmappedheader.htm
old-project: wsw
ms.assetid: f91dac8e-606e-4a9f-a598-8f8136c6b386
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsAddMappedHeader, WsAddMappedHeader function [Web Services for Windows], webservices/WsAddMappedHeader, wsw.wsaddmappedheader
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
 - WsAddMappedHeader
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsAddMappedHeader function


## -description




                Adds a specified mapped header to the <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a>.




## -parameters




### -param message [in]


                    Pointer to a <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure representing the  <a href="https://msdn.microsoft.com/edc810d9-7d78-4b79-8cbb-e87401f6ae41">message</a> to to which to add the mapped header.
                


                    The message can be in any state except <b>WS_MESSAGE_STATE_EMPTY</b> (see the <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE</a> enumeration.
                


### -param headerName [in]


                    Pointer to a <a href="https://msdn.microsoft.com/3daa656f-7f97-4e29-a556-7ff72206f01c">WS_XML_STRING</a> containing the name of the header.
                


### -param valueType [in]


                    The type of header value to deserialize.  For possible types and the corresponding headers, see the <a href="https://msdn.microsoft.com/4c9b927d-00c7-41e4-bc29-e84a4c23c162">WS_HEADER_TYPE</a>



### -param writeOption [in]


                    Whether the header is required, and how the value is allocated.
                    For more information, see the <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> enumeration.
                


### -param value [in]


                    The header value to serialize.  For more information, see  the <a href="https://msdn.microsoft.com/24a0ad2c-fcec-42c5-8f72-bea431b06d2e">WS_WRITE_OPTION</a> enumeration.
                


### -param valueSize [in]


                    The size of the value being serialized, in bytes.
                


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




                A message may contain additional transport-specific information that is
                not part of the message envelope.  This transport-specific information
                can be exposed programmatically as headers of the message.
                The <b>WsAddMappedHeader</b> function is used to add such a header that will be mapped into some
                transport-specific location.
            


                When you use the HTTP channel, you must specify the required mappings  before before you call this function to add the headers.  For more information, see <a href="https://msdn.microsoft.com/dff8217e-769d-4f0b-acf2-02d6e43589cf">WS_HTTP_MESSAGE_MAPPING</a>.
            


                If you are replacing a header, call the <a href="https://msdn.microsoft.com/aa662c92-4fb4-47af-b260-a3dedf4c6c9a">WsRemoveMappedHeader</a> function to remove
                the existing instances of the header before you call <b>WsAddMappedHeader</b>.
            



