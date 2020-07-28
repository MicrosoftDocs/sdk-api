---
UID: NF:xamlom.IVisualTreeService3.GetDictionaryItem
title: IVisualTreeService3::GetDictionaryItem (xamlom.h)
description: Gets an item from a ResourceDictionary.
helpviewer_keywords: ["GetDictionaryItem","GetDictionaryItem method","GetDictionaryItem method","IVisualTreeService3 interface","IVisualTreeService3 interface","GetDictionaryItem method","IVisualTreeService3.GetDictionaryItem","IVisualTreeService3::GetDictionaryItem","xaml_diagnostics.ivisualtreeservice3_getdictionaryitem","xamlom/IVisualTreeService3::GetDictionaryItem"]
old-location: xaml_diagnostics\ivisualtreeservice3_getdictionaryitem.htm
tech.root: xaml_diagnostics
ms.assetid: E836FE12-A49A-427C-8013-F1AFBD2C08A2
ms.date: 12/05/2018
ms.keywords: GetDictionaryItem, GetDictionaryItem method, GetDictionaryItem method,IVisualTreeService3 interface, IVisualTreeService3 interface,GetDictionaryItem method, IVisualTreeService3.GetDictionaryItem, IVisualTreeService3::GetDictionaryItem, xaml_diagnostics.ivisualtreeservice3_getdictionaryitem, xamlom/IVisualTreeService3::GetDictionaryItem
f1_keywords:
- xamlom/IVisualTreeService3.GetDictionaryItem
dev_langs:
- c++
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: XamlOM.idl
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
- xamlom.h
api_name:
- IVisualTreeService3.GetDictionaryItem
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IVisualTreeService3::GetDictionaryItem


## -description


Gets an item from a <a href="https://docs.microsoft.com/dotnet/api/system.windows.resourcedictionary?view=netframework-4.8">ResourceDictionary</a>.


## -parameters




### -param dictionaryHandle [in]

The dictionary to get the resource from.


### -param resourceName [in]

The name of the resource to get.


### -param resourceIsImplicitStyle [in]

<b>true</b> if the resource is an implicit style; otherwise, <b>false</b>.


### -param resourceHandle [out]

The resource that was retrieved.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice3">IVisualTreeService3</a>
 

 

