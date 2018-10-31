---
UID: NF:comcat.IEnumGUID.Clone
title: IEnumGUID::Clone
author: windows-sdk-content
description: Creates a new enumerator that contains the same enumeration state as the current one.
old-location: com\ienumguid_clone.htm
tech.root: com
ms.assetid: 5b12adf2-c2fe-4499-ab2a-94af6337e4a2
ms.author: windowssdkdev
ms.date: 10/30/2018
ms.keywords: Clone, Clone method [COM], Clone method [COM],IEnumGUID interface, IEnumGUID interface [COM],Clone method, IEnumGUID.Clone, IEnumGUID::Clone, _com_ienumguid_clone, com.ienumguid_clone, comcat/IEnumGUID::Clone
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: comcat.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: ComCat.idl
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
 - ComCat.h
api_name:
 - IEnumGUID.Clone
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IEnumGUID::Clone


## -description


Creates a new enumerator that contains the same enumeration state as the current one.

This method makes it possible to record a point in the enumeration sequence in order to return to that point at a later time. The caller must release this new enumerator separately from the first enumerator.


## -parameters




### -param ppenum [out]

A pointer to the cloned enumerator object.


## -returns



This method can return the standard return values E_INVALIDARG, E_OUTOFMEMORY, E_UNEXPECTED, and S_OK.




## -see-also




<a href="https://msdn.microsoft.com/4f2e0f96-a471-4883-be41-d93806461020">IEnumGUID</a>
 

 

