---
UID: NF:webservices.WsCreateError
title: WsCreateError function
author: windows-sdk-content
description: Creates an error object that can passed to functions to record rich error information.
old-location: wsw\wscreateerror.htm
old-project: wsw
ms.assetid: 0ec858f7-12a5-43cf-94a7-3838ab6d76ae
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WsCreateError, WsCreateError function [Web Services for Windows], webservices/WsCreateError, wsw.wscreateerror
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
 - WsCreateError
product: Windows
targetos: Windows
req.lib: WebServices.lib
req.dll: WebServices.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WsCreateError function


## -description



Creates an error object that can passed to functions to record rich error information.
            




## -parameters




### -param properties

An array of  <a href="https://msdn.microsoft.com/463b634f-bb15-494d-8061-c4fa0b97b990">WS_ERROR_PROPERTY</a> structures containing optional error properties.
                


### -param propertyCount [in]

The number of properties in the <i>properties</i> array.
                


### -param error

On success, a pointer that receives the address of the <a href="https://msdn.microsoft.com/d5763d93-8eff-4df8-9a8a-a58aefabcb21">WS_ERROR</a> structure representing the created error object.
                


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
One or more arguments are invalid.

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
 




## -remarks



When you no long need the error object, free it by calling  the <a href="https://msdn.microsoft.com/61da7bc2-b805-4379-a6b2-1e92374be1a0">WsFreeError</a> function.
            

By default, the
                language of any language-dependent information in the error object is  the current 
                user default UI language. However, you can change the language by setting 
                the WS_ERROR_PROPERTY_LANGID property. See the the <a href="https://msdn.microsoft.com/527e39be-c959-40db-8f0b-14dcd49a7ca7">WS_ERROR_PROPERTY_ID</a> enumeration.



