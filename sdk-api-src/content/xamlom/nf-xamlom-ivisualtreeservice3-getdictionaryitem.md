---
UID: NF:xamlom.IVisualTreeService3.GetDictionaryItem
title: IVisualTreeService3::GetDictionaryItem
author: windows-sdk-content
description: Gets an item from a ResourceDictionary.
old-location: xaml_diagnostics\ivisualtreeservice3_getdictionaryitem.htm
tech.root: xaml_diagnostics
ms.assetid: E836FE12-A49A-427C-8013-F1AFBD2C08A2
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetDictionaryItem, GetDictionaryItem method, GetDictionaryItem method,IVisualTreeService3 interface, IVisualTreeService3 interface,GetDictionaryItem method, IVisualTreeService3.GetDictionaryItem, IVisualTreeService3::GetDictionaryItem, xaml_diagnostics.ivisualtreeservice3_getdictionaryitem, xamlom/IVisualTreeService3::GetDictionaryItem
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualTreeService3::GetDictionaryItem


## -description


Gets an item from a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>.


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




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

