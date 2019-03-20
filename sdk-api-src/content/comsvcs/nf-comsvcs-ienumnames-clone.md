---
UID: NF:comsvcs.IEnumNames.Clone
title: IEnumNames::Clone (comsvcs.h)
author: windows-sdk-content
description: Creates an enumerator that contains the same enumeration state as the current one.
old-location: cos\ienumnames_clone.htm
tech.root: cossdk
ms.assetid: ea57be73-076a-445d-9b0d-4a1041befa2d
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: Clone, Clone method [COM+], Clone method [COM+],IEnumNames interface, IEnumNames interface [COM+],Clone method, IEnumNames.Clone, IEnumNames::Clone, _cos_IEnumNames_Clone, comsvcs/IEnumNames::Clone, cos.ienumnames_clone
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
 - IEnumNames.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumNames::Clone


## -description


Creates an enumerator that contains the same enumeration state as the current one.


## -parameters




### -param ppenum [out]

Address of a pointer to the <a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a> interface on the enumeration object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, E_FAIL, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/9f70b554-3cdd-4a4b-b180-c6de6182a46a">IEnumNames</a>
 

 

