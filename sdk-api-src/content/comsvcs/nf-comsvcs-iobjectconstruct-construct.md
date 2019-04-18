---
UID: NF:comsvcs.IObjectConstruct.Construct
title: IObjectConstruct::Construct (comsvcs.h)
author: windows-sdk-content
description: Constructs an object using the specified parameters.
old-location: cos\iobjectconstruct_construct.htm
tech.root: cossdk
ms.assetid: 6bbb25c7-bd60-46cb-baed-114c50feb1f3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: Construct, Construct method [COM+], Construct method [COM+],IObjectConstruct interface, IObjectConstruct interface [COM+],Construct method, IObjectConstruct.Construct, IObjectConstruct::Construct, _cos_IObjectConstruct_Construct, comsvcs/IObjectConstruct::Construct, cos.iobjectconstruct_construct
ms.topic: method
req.header: comsvcs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
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
 - COM
api_location:
 - ComSvcs.h
api_name:
 - IObjectConstruct.Construct
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IObjectConstruct::Construct


## -description


Constructs an object using the specified parameters.


## -parameters




### -param pCtorObj [in]

A reference to an implementation of the <a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a> interface. 


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/5e630812-b2cf-4512-af67-6e919a02bf95">COM+ Object Constructor Strings</a>



<a href="https://msdn.microsoft.com/3fc84c37-f38d-4ff1-bdb1-f5d298802b64">IObjectConstruct</a>



<a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a>



<a href="https://msdn.microsoft.com/0c5aaaae-368e-4b3e-a483-b3a23c353e6e">Specifying an Object Constructor String for a Component</a>
 

 

