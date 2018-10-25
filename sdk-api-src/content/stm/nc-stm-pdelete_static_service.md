---
UID: NC:stm.PDELETE_STATIC_SERVICE
title: PDELETE_STATIC_SERVICE
author: windows-sdk-content
description: The DeleteStaticService function deletes a static service from the table.
old-location: rras\deletestaticservice.htm
tech.root: rras
ms.assetid: 230ddff5-7fd1-4e4e-b4bb-49c427a3f9c7
ms.author: windowssdkdev
ms.date: 10/24/2018
ms.keywords: DeleteStaticService, DeleteStaticService callback function [RAS], PDELETE_STATIC_SERVICE, PDELETE_STATIC_SERVICE callback, _mpr_deletestaticservice, rras.deletestaticservice, stm/DeleteStaticService
ms.prod: windows
ms.technology: windows-sdk
ms.topic: callback
req.header: stm.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Stm.h
api_name:
 - DeleteStaticService
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PDELETE_STATIC_SERVICE callback function


## -description


The 
<b>DeleteStaticService</b> function deletes a static service from the table.


## -parameters




### -param InterfaceIndex [in]

Specifies a unique number that identifies the interface associated with the service intended for deletion.


### -param ServerEntry








#### - ServiceEntry [in]

Pointer to an 
<a href="https://msdn.microsoft.com/873a3808-9813-43b4-818a-bea7e1fb7cd3">IPX_STATIC_SERVICE_INFO</a> structure that specifies the parameters of the static service intended for deletion.


## -returns



If the function succeeds, the return value is NO_ERROR.

If the function fails, the return value is one of the following error codes.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_CAN_NOT_COMPLETE</b></dt>
</dl>
</td>
<td width="60%">
The SAP Agent is down.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One of the  parameters is invalid.

</td>
</tr>
</table>
 


<div> </div>





## -see-also




<a href="https://msdn.microsoft.com/529beae6-ba39-417c-8fa6-7b97fc720352">CreateStaticService</a>



<a href="https://msdn.microsoft.com/e93e3bf2-80a2-44ec-a067-58220cdd31b4">IPX Service Table Management</a>



<a href="https://msdn.microsoft.com/873a3808-9813-43b4-818a-bea7e1fb7cd3">IPX_STATIC_SERVICE_INFO</a>



<a href="https://msdn.microsoft.com/eb31f1ad-5761-4112-8c05-51a627b9e0b7">Service Table Management Functions</a>
 

 

