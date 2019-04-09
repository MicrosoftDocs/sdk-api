---
UID: NF:webservices.WsGetListenerProperty
title: WsGetListenerProperty function (webservices.h)
author: windows-sdk-content
description: Retrieves a specified Listener object property. The property to retrieve is identified by a WS_LISTENER_PROPERTY_ID input parameter.
old-location: wsw\wsgetlistenerproperty.htm
tech.root: wsw
ms.assetid: cc4fb48a-8282-471a-aed0-1ca3134f9bd0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WsGetListenerProperty, WsGetListenerProperty function [Web Services for Windows], webservices/WsGetListenerProperty, wsw.wsgetlistenerproperty
ms.topic: function
req.header: webservices.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WebServices.dll
api_name:
 - WsGetListenerProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsGetListenerProperty function


## -description


Retrieves a specified Listener object  property.  The property to retrieve is identified by a  <a href="https://msdn.microsoft.com/52e4a5d3-e584-40d1-b71f-b4ef61104883">WS_LISTENER_PROPERTY_ID</a> input parameter.
            


## -parameters




### -param listener [in]

A pointer to the Listener object containing the desired property.  This must be a valid <a href="https://msdn.microsoft.com/2e771c56-4a07-4c8e-92c1-ffcbf74cd1aa">WS_LISTENER</a> that was returned
                    from <a href="https://msdn.microsoft.com/2e592fd2-cf88-4f87-a71b-1c3416917fa7">WsCreateListener</a>.  


### -param id [in]

This is a <b>WS_LISTENER_PROPERTY_ID</b> enumerator value that identifies the desired property.
                


### -param value

A reference to a location for storing the retrieved property value.
                    The pointer must have an alignment compatible with the type
                    of the property.
                


### -param valueSize [in]

Represents the byte-length buffer size allocated by the caller to store the retrieved property value.
                


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
The property id was not supported for this object or the specified buffer was not large enough for the value.

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
 



