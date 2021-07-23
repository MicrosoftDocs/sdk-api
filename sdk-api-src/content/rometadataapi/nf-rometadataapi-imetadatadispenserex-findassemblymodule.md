---
UID: NF:rometadataapi.IMetaDataDispenserEx.FindAssemblyModule
title: IMetaDataDispenserEx::FindAssemblyModule (rometadataapi.h)
description: Finds the name of the assembly module.
helpviewer_keywords: ["FindAssemblyModule","FindAssemblyModule method [Windows Runtime]","FindAssemblyModule method [Windows Runtime]","IMetaDataDispenserEx interface","IMetaDataDispenserEx interface [Windows Runtime]","FindAssemblyModule method","IMetaDataDispenserEx.FindAssemblyModule","IMetaDataDispenserEx::FindAssemblyModule","rometadataapi/IMetaDataDispenserEx::FindAssemblyModule","winrt.imetadatadispenserex_findassemblymodule"]
old-location: winrt\imetadatadispenserex_findassemblymodule.htm
tech.root: WinRT
ms.assetid: 258d670b-6a94-4151-8746-a3df69677c5b
ms.date: 12/05/2018
ms.keywords: FindAssemblyModule, FindAssemblyModule method [Windows Runtime], FindAssemblyModule method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],FindAssemblyModule method, IMetaDataDispenserEx.FindAssemblyModule, IMetaDataDispenserEx::FindAssemblyModule, rometadataapi/IMetaDataDispenserEx::FindAssemblyModule, winrt.imetadatadispenserex_findassemblymodule
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMetaDataDispenserEx::FindAssemblyModule
 - rometadataapi/IMetaDataDispenserEx::FindAssemblyModule
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - rometadataapi.h
api_name:
 - IMetaDataDispenserEx.FindAssemblyModule
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

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>