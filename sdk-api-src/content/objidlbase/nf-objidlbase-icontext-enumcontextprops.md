---
UID: NF:objidlbase.IContext.EnumContextProps
title: IContext::EnumContextProps
author: windows-sdk-content
description: Returns an IEnumContextProps interface pointer that can be used to enumerate the context properties in this context.
old-location: com\icontext_enumcontextprops.htm
old-project: com
ms.assetid: 7cae291e-dcf3-43b1-8306-9e5c7a5d3be0
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: EnumContextProps, EnumContextProps method [COM], EnumContextProps method [COM],IContext interface, IContext interface [COM],EnumContextProps method, IContext.EnumContextProps, IContext::EnumContextProps, _com_icontext_enumcontextprops, com.icontext_enumcontextprops, objidlbase/IContext::EnumContextProps
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: objidlbase.h
req.include-header: ObjIdl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ObjIdl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: THDTYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - objidlbase.h
api_name:
 - IContext.EnumContextProps
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IContext::EnumContextProps


## -description


Returns an <a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a> interface pointer that can be used to enumerate the context properties in this context.


## -parameters




### -param ppEnumContextProps [out]

The address of the variable that receives the new <a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a> interface pointer.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/89c41d9c-186c-4927-990d-92aa501f7d35">IContext</a>



<a href="https://msdn.microsoft.com/64591e45-5478-4360-8c1f-08b09b5aef8e">IEnumContextProps</a>
 

 

