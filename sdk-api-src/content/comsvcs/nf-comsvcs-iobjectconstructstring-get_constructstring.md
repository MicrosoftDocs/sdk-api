---
UID: NF:comsvcs.IObjectConstructString.get_ConstructString
title: IObjectConstructString::get_ConstructString
author: windows-sdk-content
description: Retrieves the constructor string for the object.
old-location: cos\iobjectconstructstring_get_constructstring.htm
tech.root: cossdk
ms.assetid: 154b7567-0f25-49c3-90b2-58c95f0ebfee
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IObjectConstructString interface [COM+],get_ConstructString method, IObjectConstructString.get_ConstructString, IObjectConstructString::get_ConstructString, _cos_IObjectConstructString_get_ConstructString, comsvcs/IObjectConstructString::get_ConstructString, cos.iobjectconstructstring_get_constructstring, get_ConstructString, get_ConstructString method [COM+], get_ConstructString method [COM+],IObjectConstructString interface
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IObjectConstructString.get_ConstructString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- comsvcs.h
: 
- IObjectConstructString.get_ConstructString
: 
---

# IObjectConstructString::get_ConstructString


## -description


Retrieves the constructor string for the object.

Object constructor strings should not be used to store security-sensitive information.


## -parameters




### -param pVal [out]

A reference to an administratively supplied object constructor string.



## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -remarks



You can use this method when implementing <a href="https://msdn.microsoft.com/6bbb25c7-bd60-46cb-baed-114c50feb1f3">IObjectConstruct::Construct</a>, which is called by the COM+ environment when your component is marked as supporting object construction. 





## -see-also




<a href="https://msdn.microsoft.com/5e630812-b2cf-4512-af67-6e919a02bf95">COM+ Object Constructor Strings</a>



<a href="https://msdn.microsoft.com/3fc84c37-f38d-4ff1-bdb1-f5d298802b64">IObjectConstruct</a>



<a href="https://msdn.microsoft.com/ebfa8384-1efd-4775-b66f-b8048af33abc">IObjectConstructString</a>



<a href="https://msdn.microsoft.com/0c5aaaae-368e-4b3e-a483-b3a23c353e6e">Specifying an Object Constructor String for a Component</a>
 

 

