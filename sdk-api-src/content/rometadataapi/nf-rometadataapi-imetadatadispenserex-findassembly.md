---
UID: NF:rometadataapi.IMetaDataDispenserEx.FindAssembly
title: IMetaDataDispenserEx::FindAssembly (rometadataapi.h)
author: windows-sdk-content
description: Gets the name of the assembly.
old-location: winrt\imetadatadispenserex_findassembly.htm
tech.root: WinRT
ms.assetid: 7f691157-9f3d-4e04-91ee-9d62c23569d8
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: FindAssembly, FindAssembly method [Windows Runtime], FindAssembly method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],FindAssembly method, IMetaDataDispenserEx.FindAssembly, IMetaDataDispenserEx::FindAssembly, rometadataapi/IMetaDataDispenserEx::FindAssembly, winrt.imetadatadispenserex_findassembly
ms.topic: method
f1_keywords: ["rometadataapi/IMetaDataDispenserEx.FindAssembly"]
req.header: rometadataapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Rometadataapi.idl
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
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx.FindAssembly
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataDispenserEx::FindAssembly


## -description


Gets the name of the assembly.


## -parameters




### -param szAppBase [in]

Not used.


### -param szPrivateBin [in]

Not used.


### -param szGlobalBin [in]

Not used.


### -param szAssemblyName [in]

The name of the assembly to find.


### -param szName [out]

The simple name of the assembly.


### -param cchName [in]

The size, in bytes, of <i>szName</i>.


### -param pchName [out]

The number of characters actually returned in <i>szName</i>.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>
 

 

