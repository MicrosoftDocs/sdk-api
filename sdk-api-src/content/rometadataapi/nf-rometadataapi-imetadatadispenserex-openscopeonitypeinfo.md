---
UID: NF:rometadataapi.IMetaDataDispenserEx.OpenScopeOnITypeInfo
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo
author: windows-sdk-content
description: Opens the specified scope type.
old-location: winrt\imetadatadispenserex_openscopeonitypeinfo.htm
old-project: WinRT
ms.assetid: e76d295a-bce9-42c2-9a9b-a4d31741f47f
ms.author: windowssdkdev
ms.date: 05/15/2018
ms.keywords: IMetaDataDispenserEx interface [Windows Runtime],OpenScopeOnITypeInfo method, IMetaDataDispenserEx.OpenScopeOnITypeInfo, IMetaDataDispenserEx::OpenScopeOnITypeInfo, OpenScopeOnITypeInfo, OpenScopeOnITypeInfo method [Windows Runtime], OpenScopeOnITypeInfo method [Windows Runtime],IMetaDataDispenserEx interface, rometadataapi/IMetaDataDispenserEx::OpenScopeOnITypeInfo, winrt.imetadatadispenserex_openscopeonitypeinfo
ms.prod: windows
ms.technology: windows-sdk
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
-	IMetaDataDispenserEx.OpenScopeOnITypeInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# IMetaDataDispenserEx::OpenScopeOnITypeInfo


## -description


Opens the specified scope type.


## -parameters




### -param pITI [in]

Pointer to an <a href="http://msdn.microsoft.com/en-us/library/f3356463-3373-4279-bae1-953378aa2680(VS.85)">ITypeInfo</a> interface that provides the type information on which to open the scope.


### -param dwOpenFlags [in]

The open mode flags.


### -param riid [in]

The desired interface.


### -param ppIUnk [out]

Pointer to a pointer to the returned interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/b61c8d05-6d73-4f84-95b2-2a892f3de77c">IMetaDataDispenserEx</a>
 

 

