---
UID: NF:webservices.WsGetFaultErrorProperty
title: WsGetFaultErrorProperty function
author: windows-sdk-content
description: Retrieves a Fault error property of an WS_ERROR object referenced by the error parameter.
old-location: wsw\wsgetfaulterrorproperty.htm
tech.root: wsw
ms.assetid: b59e6ac6-a3f1-4a72-a941-f588950ba85a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: WsGetFaultErrorProperty, WsGetFaultErrorProperty function [Web Services for Windows], webservices/WsGetFaultErrorProperty, wsw.wsgetfaulterrorproperty
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - WsGetFaultErrorProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# WsGetFaultErrorProperty function


## -description


Retrieves a <a href="https://msdn.microsoft.com/7fe0b142-04a1-4a92-99ca-523412f7c94e">Fault</a> error property of an <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object referenced by the <i>error</i> parameter.


## -parameters




### -param error [in]

A pointer to the  <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> object with the property to retrieve.  
                    
                


### -param id [in]

Represents an identifier of the fault error property to retrieve.
                


### -param buffer

A pointer referencing the location to store the retrieved fault error property.
                    

<div class="alert"><b>Note</b>  The pointer must have an alignment compatible with the type
                    of the property.</div>
<div> </div>

### -param bufferSize [in]

The number of bytes allocated by the caller to
                    store the retrieved property.
                


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
 



