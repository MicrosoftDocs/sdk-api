---
UID: NF:rometadataapi.IMetaDataDispenserEx.FindAssemblyModule
title: IMetaDataDispenserEx::FindAssemblyModule
author: windows-driver-content
description: Finds the name of the assembly module.
old-location: winrt\imetadatadispenserex_findassemblymodule.htm
old-project: WinRT
ms.assetid: 258d670b-6a94-4151-8746-a3df69677c5b
ms.author: windowsdriverdev
ms.date: 5/15/2018
ms.keywords: FindAssemblyModule, FindAssemblyModule method [Windows Runtime], FindAssemblyModule method [Windows Runtime],IMetaDataDispenserEx interface, IMetaDataDispenserEx interface [Windows Runtime],FindAssemblyModule method, IMetaDataDispenserEx.FindAssemblyModule, IMetaDataDispenserEx::FindAssemblyModule, rometadataapi/IMetaDataDispenserEx::FindAssemblyModule, winrt.imetadatadispenserex_findassemblymodule
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: RO_ERROR_REPORTING_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	rometadataapi.h
api_name:
-	IMetaDataDispenserEx.FindAssemblyModule
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

