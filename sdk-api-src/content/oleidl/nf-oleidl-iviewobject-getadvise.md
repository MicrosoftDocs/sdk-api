---
UID: NF:oleidl.IViewObject.GetAdvise
title: IViewObject::GetAdvise
author: windows-sdk-content
description: Retrieves the advisory connection on the object that was used in the most recent call to IViewObject::SetAdvise.
old-location: com\iviewobject_getadvise.htm
old-project: com
ms.assetid: c56f6cbb-d2ea-4db4-a660-db8b7540ac94
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: GetAdvise, GetAdvise method [COM], GetAdvise method [COM],IViewObject interface, IViewObject interface [COM],GetAdvise method, IViewObject.GetAdvise, IViewObject::GetAdvise, _ole_iviewobject_getadvise, com.iviewobject_getadvise, oleidl/IViewObject::GetAdvise
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: oleidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OleIdl.Idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: USERCLASSTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OleIdl.h
api_name:
 - IViewObject.GetAdvise
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
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
 

 

