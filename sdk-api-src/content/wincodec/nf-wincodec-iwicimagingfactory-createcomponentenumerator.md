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

# IWICImagingFactory::CreateComponentEnumerator


## -description


Creates an <a href="_com_IEnumUnknown">IEnumUnknown</a> object of the specified component types.


## -parameters




### -param componentTypes [in]

Type: <b>DWORD</b>

The types of <a href="https://msdn.microsoft.com/eff6b77c-ea4b-4476-8d75-dec5bb2e1745">WICComponentType</a> to enumerate.


### -param options [in]

Type: <b>DWORD</b>

The <a href="https://msdn.microsoft.com/52cc0860-6164-4400-8e81-03eb0c44904e">WICComponentEnumerateOptions</a> used to enumerate the given component types. 


### -param ppIEnumUnknown [out]

Type: <b><a href="_com_IEnumUnknown">IEnumUnknown</a>**</b>

A pointer that receives a pointer to a new component enumerator.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Component types must be enumerated seperately. Combinations of component types and <b>WICAllComponents</b> are unsupported.



