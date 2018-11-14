---
UID: NF:xamlom.IVisualTreeService3.AddDictionaryItem
title: IVisualTreeService3::AddDictionaryItem
author: windows-sdk-content
description: Adds an item to a ResourceDictionary, and re-resolves all elements in the tree that reference a resource with the specified key.
old-location: xaml_diagnostics\ivisualtreeservice3_adddictionaryitem.htm
tech.root: xaml_diagnostics
ms.assetid: 86590A71-8BFC-4214-9F7C-1DF5B8391552
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: AddDictionaryItem, AddDictionaryItem method, AddDictionaryItem method,IVisualTreeService3 interface, IVisualTreeService3 interface,AddDictionaryItem method, IVisualTreeService3.AddDictionaryItem, IVisualTreeService3::AddDictionaryItem, xaml_diagnostics.ivisualtreeservice3_adddictionaryitem, xamlom/IVisualTreeService3::AddDictionaryItem
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - IVisualTreeService3.AddDictionaryItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- xamlom.h
: 
- IVisualTreeService3.AddDictionaryItem
: 
---

# IVisualTreeService3::AddDictionaryItem


## -description


	Adds an item to a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.


## -parameters




### -param dictionaryHandle [in]

The dictionary to add the resource to.


### -param resourceKey [in]

The key of the resource to add.


### -param resourceHandle [in]

The resource to add.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any invalid resource references will result in the value being cleared, and <a href="https://msdn.microsoft.com/F1C11F32-9524-49D6-89DD-C89E4A81720A">IVisualTreeServiceCallback2</a>  will be notified.




## -see-also




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

