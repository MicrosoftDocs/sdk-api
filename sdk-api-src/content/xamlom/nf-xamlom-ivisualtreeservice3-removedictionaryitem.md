---
UID: NF:xamlom.IVisualTreeService3.RemoveDictionaryItem
title: IVisualTreeService3::RemoveDictionaryItem (xamlom.h)
description: Removes an item from a ResourceDictionary, and re-resolves all elements in the tree that reference a resource with the specified key.
helpviewer_keywords: ["IVisualTreeService3 interface","RemoveDictionaryItem method","IVisualTreeService3.RemoveDictionaryItem","IVisualTreeService3::RemoveDictionaryItem","RemoveDictionaryItem","RemoveDictionaryItem method","RemoveDictionaryItem method","IVisualTreeService3 interface","xaml_diagnostics.ivisualtreeservice3_removedictionaryitem","xamlom/IVisualTreeService3::RemoveDictionaryItem"]
old-location: xaml_diagnostics\ivisualtreeservice3_removedictionaryitem.htm
tech.root: xaml_diagnostics
ms.assetid: 6239D855-7408-47ED-9090-E7726E7E403E
ms.date: 08/03/2022
ms.keywords: IVisualTreeService3 interface,RemoveDictionaryItem method, IVisualTreeService3.RemoveDictionaryItem, IVisualTreeService3::RemoveDictionaryItem, RemoveDictionaryItem, RemoveDictionaryItem method, RemoveDictionaryItem method,IVisualTreeService3 interface, xaml_diagnostics.ivisualtreeservice3_removedictionaryitem, xamlom/IVisualTreeService3::RemoveDictionaryItem
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IVisualTreeService3::RemoveDictionaryItem
 - xamlom/IVisualTreeService3::RemoveDictionaryItem
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - xamlom.h
api_name:
 - IVisualTreeService3.RemoveDictionaryItem
---

# IVisualTreeService3::RemoveDictionaryItem


## -description

	Removes an item from a <a href="/dotnet/api/system.windows.resourcedictionary?view=netframework-4.8&preserve-view=true">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.

## -parameters

### -param dictionaryHandle [in]

The dictionary to remove the resource from.

### -param resourceKey [in]

The key of the resource to remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Any invalid resource references will result in the value being cleared, and <a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservicecallback2">IVisualTreeServiceCallback2</a>  will be notified.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice3">IVisualTreeService3</a>