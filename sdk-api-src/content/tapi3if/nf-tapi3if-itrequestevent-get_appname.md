---
UID: NF:tapi3if.ITRequestEvent.get_AppName
title: ITRequestEvent::get_AppName
author: windows-sdk-content
description: The get_AppName method gets the name of the application.
old-location: tapi3\itrequestevent_get_appname.htm
old-project: tapi
ms.assetid: d53fae21-4a4d-46ab-a0ff-48a7474b8782
ms.author: windowssdkdev
ms.date: 05/28/2018
ms.keywords: ITRequestEvent interface [TAPI 2.2],get_AppName method, ITRequestEvent.get_AppName, ITRequestEvent::get_AppName, _tapi3_itrequestevent_get_appname, get_AppName, get_AppName method [TAPI 2.2], get_AppName method [TAPI 2.2],ITRequestEvent interface, tapi3.itrequestevent_get_appname, tapi3if/ITRequestEvent::get_AppName
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: tapi3if.h
req.include-header: Tapi3.h
req.target-type: Windows
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
tech.root: 
req.typenames: TERMINAL_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITRequestEvent.get_AppName
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# ITRequestEvent::get_AppName


## -description


The 
<b>get_AppName</b> method gets the name of the application.


## -parameters




### -param ppAppName [out]

Pointer to a <b>BSTR</b> containing the application name.


## -returns



This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppAppName</i> is not a valid pointer.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
</table>
 




## -remarks



The application must use 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> to free the memory allocated for the <i>ppAppName</i> parameter.
			




## -see-also




<a href="https://msdn.microsoft.com/69f9b504-be01-4167-8002-32a8e86bab0f">ITRequestEvent</a>
 

 

