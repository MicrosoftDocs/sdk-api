---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ISdo::get__NewEnum


## -description


The 
<b>get__NewEnum</b> method retrieves an 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface for the Server Data Objects (SDO) properties.


## -parameters




### -param ppEnumVARIANT [out]

Pointer to a pointer that, on successful return, points to an 
<a href="_com_iunknown">IUnknown</a> interface pointer. Use this <b>IUnknown</b> interface pointer with 
its <a href="_com_iunknown_queryinterface">QueryInterface</a> method to obtain an 
<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a> interface.


## -returns



If the method succeeds the return value is <b>S_OK</b>.

If the method fails, the return value is one of the following error codes.




## -remarks



<div class="alert"><b>Note</b>  Two underscores are used between "get" and "NewEnum" in the name of this method.</div>
<div> </div>



## -see-also




<a href="139e3c93-faef-4003-9079-e0e94494db3e">IEnumVARIANT</a>



<a href="https://msdn.microsoft.com/f8f49bf2-d8cc-40ad-ac52-05d74bcd931c">ISdo</a>
 

 

