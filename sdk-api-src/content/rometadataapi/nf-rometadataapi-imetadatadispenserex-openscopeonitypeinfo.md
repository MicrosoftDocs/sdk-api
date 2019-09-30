---
UID: NF:rometadataapi.IMetaDataDispenserEx.OpenScopeOnITypeInfo
title: IMetaDataDispenserEx::OpenScopeOnITypeInfo (rometadataapi.h)
author: windows-sdk-content
description: Opens the specified scope type.
old-location: winrt\imetadatadispenserex_openscopeonitypeinfo.htm
tech.root: WinRT
ms.assetid: e76d295a-bce9-42c2-9a9b-a4d31741f47f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IMetaDataDispenserEx interface [Windows Runtime],OpenScopeOnITypeInfo method, IMetaDataDispenserEx.OpenScopeOnITypeInfo, IMetaDataDispenserEx::OpenScopeOnITypeInfo, OpenScopeOnITypeInfo, OpenScopeOnITypeInfo method [Windows Runtime], OpenScopeOnITypeInfo method [Windows Runtime],IMetaDataDispenserEx interface, rometadataapi/IMetaDataDispenserEx::OpenScopeOnITypeInfo, winrt.imetadatadispenserex_openscopeonitypeinfo
ms.topic: method
f1_keywords: 
 - "rometadataapi/IMetaDataDispenserEx.OpenScopeOnITypeInfo"
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
 - IMetaDataDispenserEx.OpenScopeOnITypeInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IMetaDataDispenserEx::OpenScopeOnITypeInfo


## -description


Opens the specified scope type.


## -parameters




### -param pITI [in]

Pointer to an <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/oaidl/nn-oaidl-itypeinfo">ITypeInfo</a> interface that provides the type information on which to open the scope.


### -param dwOpenFlags [in]

The open mode flags.


### -param riid [in]

The desired interface.


### -param ppIUnk [out]

Pointer to a pointer to the returned interface.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/rometadataapi/nn-rometadataapi-imetadatadispenserex">IMetaDataDispenserEx</a>
 

 

