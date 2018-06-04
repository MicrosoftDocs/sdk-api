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

# IMetaDataDispenserEx::FindAssemblyModule


## -description


Finds the name of the assembly module.


## -parameters




### -param szAppBase [in]

Not used.


### -param szPrivateBin [in]

Not used.


### -param szGlobalBin [in]

Not used.


### -param szAssemblyName [in]

The assembly to be found.


### -param szModuleName [in]

The name of the module.


### -param szName [out]

The simple name of the assembly.


### -param cchName [in]

The size, in bytes, of <i>szName</i>.


### -param pcName [out]

The number of characters actually returned in <i>szName</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b61c8d05-6d73-4f84-95b2-2a892f3de77c">IMetaDataDispenserEx</a>
 

 

