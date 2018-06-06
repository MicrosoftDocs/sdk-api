---
UID: NF:webservices.WsCreateServiceHost
title: WsCreateServiceHost function
author: windows-sdk-content
description: Creates a service host for the specified endpoints.
old-location: wsw\wscreateservicehost.htm
old-project: wsw
ms.assetid: 412a262a-1706-4101-b154-1804408a5b9f
ms.author: windowssdkdev
ms.date: 05/18/2018
ms.keywords: WsCreateServiceHost, WsCreateServiceHost function [Web Services for Windows], webservices/WsCreateServiceHost, wsw.wscreateservicehost
ms.prod: windows
ms.technology: windows-sdk
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
 - WsCreateServiceHost
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateServiceHost function


## -description




                Creates a <a href="https://msdn.microsoft.com/42e4d24d-5611-4561-b874-6dc3f3f88c73">service host</a> for the specified endpoints.
            




## -parameters




### -param endpoints

An array of  <a href="https://msdn.microsoft.com/6b15fc3f-5e4b-4eb3-b337-0170b0ca746f">WS_SERVICE_ENDPOINT</a> structures representing the service endpoints for which to create the service host.


### -param endpointCount [in]


                    The number of endpoints in the <i>endpoints</i> array.
                


### -param serviceProperties

An array of <a href="https://msdn.microsoft.com/d25cab25-2227-4afe-ae45-93a229d7f78b">WS_SERVICE_PROPERTY</a> structures containing optional properties for the service host.

The value of this parameter may be <b>NULL</b>, in which case, the <i>servicePropertyCount</i> parameter must be 0 (zero).
                


### -param servicePropertyCount [in]

The number of properties in the <i>serviceProperties</i> array.
                


### -param serviceHost


                    On   success, a pointer that receives the address of the  <a href="https://msdn.microsoft.com/1186e3ae-87d0-4d0b-a7cc-cce63dc091e2">WS_SERVICE_HOST</a> structure representing the new service host.
                
                When you no longer need this structure, you must free it by calling <a href="https://msdn.microsoft.com/5362d8a4-8b38-462a-a7c1-9cde19abee1e">WsFreeServiceHost</a>.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
An invalid argument is specified for creating the service host.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>WS_E_QUOTA_EXCEEDED</b></dt>
</dl>
</td>
<td width="60%">

A quota was exceeded.

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
<dt><b> Other Errors </b></dt>
</dl>
</td>
<td width="60%">
This function may return other errors not listed above.

</td>
</tr>
</table>
 



