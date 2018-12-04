---
UID: NF:tapi3cc.ITAgentHandler.get_Name
title: ITAgentHandler::get_Name
author: windows-sdk-content
description: The get_Name method gets the agent handler name.
old-location: tapi3\itagenthandler_get_name.htm
tech.root: tapi
ms.assetid: 18596742-9a0e-44c1-97e1-1d13d84cc10c
ms.author: windowssdkdev
ms.date: 11/23/2018
ms.keywords: ITAgentHandler interface [TAPI 2.2],get_Name method, ITAgentHandler.get_Name, ITAgentHandler::get_Name, _tapi3_itagenthandler_get_name, get_Name, get_Name method [TAPI 2.2], get_Name method [TAPI 2.2],ITAgentHandler interface, tapi3.itagenthandler_get_name, tapi3cc/ITAgentHandler::get_Name
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: tapi3cc.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITAgentHandler.get_Name
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ITAgentHandler::get_Name


## -description


The 
<b>get_Name</b> method gets the agent handler name.


## -parameters




### -param ppName [out]

Pointer to <b>BSTR</b> representation of the agent handler name.


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
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform the operation.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_POINTER</b></dt>
</dl>
</td>
<td width="60%">
The <i>ppName</i> parameter is not a valid pointer.

</td>
</tr>
</table>
 




## -remarks



The application must free the memory allocated for the <i>ppName</i> parameter through 
<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when the variable is no longer needed.




## -see-also




<a href="https://msdn.microsoft.com/11861d77-39ad-4d85-bf68-ba0f4321ba7c">ITAgentHandler</a>
 

 

