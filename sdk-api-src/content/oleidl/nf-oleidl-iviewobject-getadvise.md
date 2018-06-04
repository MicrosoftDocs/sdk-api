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

# IViewObject::GetAdvise


## -description


Retrieves the advisory connection on the object that was used in the most recent call to <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>.


## -parameters




### -param pAspects [out]

Pointer to where the <i>dwAspect</i> parameter from the previous <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a> call is returned. If this pointer is <b>NULL</b>, the caller does not permit this value to be returned.


### -param pAdvf [out]

Pointer to where the <i>advf</i> parameter from the previous <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a> call is returned. If this pointer is <b>NULL</b>, the caller does not permit this value to be returned.


### -param ppAdvSink [out]

Address of <a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a> pointer variable that receives the interface pointer to the advise sink. The connection to this advise sink must have been established with a previous <a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a> call, which provides the <i>pAdvSink</i> parameter. If <i>ppvAdvSink</i> is <b>NULL</b>, there is no established advisory connection.


## -returns



This method returns S_OK on success.




## -see-also




<a href="https://msdn.microsoft.com/e1ad9c17-e492-4891-bf1d-cbac48ce537a">ADVF</a>



<a href="https://msdn.microsoft.com/bc9f217a-75bd-4155-9d00-df44b00cf0e5">IAdviseSink</a>



<a href="https://msdn.microsoft.com/4310c987-3542-4a59-a6fb-951143001741">IViewObject</a>



<a href="https://msdn.microsoft.com/64712679-8454-41fa-9497-f0ab97240a51">IViewObject::SetAdvise</a>
 

 

