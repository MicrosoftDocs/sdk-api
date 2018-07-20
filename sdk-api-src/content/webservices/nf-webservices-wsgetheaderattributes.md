---
UID: NF:webservices.WsGetHeaderAttributes
title: WsGetHeaderAttributes function
author: windows-sdk-content
description: This function populates a ULONG parameter with the WS_HEADER_ATTRIBUTES from the header element on which the reader is positioned. The envelope version of the message is used to determine which attributes to return.
old-location: wsw\wsgetheaderattributes.htm
old-project: wsw
ms.assetid: 323178d4-6bc9-4b5e-bd3d-b36972720cd7
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: WsGetHeaderAttributes, WsGetHeaderAttributes function [Web Services for Windows], webservices/WsGetHeaderAttributes, wsw.wsgetheaderattributes
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps \| UWP apps]
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
 - WsGetHeaderAttributes
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsGetHeaderAttributes function


## -description



                This function populates a ULONG parameter with  the <a href="https://msdn.microsoft.com/2796253d-3b8d-490d-987d-5bf7cd48c8ea">WS_HEADER_ATTRIBUTES</a> from the header element on which the reader is positioned.  The
                envelope version of the message is used to determine which attributes to return.
            


## -parameters




### -param message [in]

A  pointer to a <a href="https://msdn.microsoft.com/22cc39a9-a3a7-4b4d-bdee-0ccac5dc03ee">WS_MESSAGE</a> structure containing the message to query.  This envelope version of the message is used to determine which attributes match.
                The message can be in any state except <a href="https://msdn.microsoft.com/2c5ddedd-b0b4-4c26-a5c0-a5851f0408de">WS_MESSAGE_STATE_EMPTY</a>.


### -param reader [in]


          A pointer to the reader to query.  This must be valid WS_XML_READER object returned from <a href="https://msdn.microsoft.com/0d4449aa-ffcc-41d9-99b1-7352edaf3700">WsCreateReader</a>   and cannot be <b>NULL</b>.
        


### -param headerAttributes [out]

On success the value referenced by this pointer is set to the header attributes.
                


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">

Ran out of memory.

</td>
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
<dt><b>WS_E_INVALID_FORMAT</b></dt>
</dl>
</td>
<td width="60%">

The input data was not in the expected format or did not have the expected value.

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




                The reader is assumed to point to a header element.  Use the XML reader API's to position the reader appropriately.
            



