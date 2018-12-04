---
UID: NF:xamlom.IVisualTreeService3.RemoveDictionaryItem
title: IVisualTreeService3::RemoveDictionaryItem
author: windows-sdk-content
description: Removes an item from a ResourceDictionary, and re-resolves all elements in the tree that reference a resource with the specified key.
old-location: xaml_diagnostics\ivisualtreeservice3_removedictionaryitem.htm
tech.root: xaml_diagnostics
ms.assetid: 6239D855-7408-47ED-9090-E7726E7E403E
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IVisualTreeService3 interface,RemoveDictionaryItem method, IVisualTreeService3.RemoveDictionaryItem, IVisualTreeService3::RemoveDictionaryItem, RemoveDictionaryItem, RemoveDictionaryItem method, RemoveDictionaryItem method,IVisualTreeService3 interface, xaml_diagnostics.ivisualtreeservice3_removedictionaryitem, xamlom/IVisualTreeService3::RemoveDictionaryItem
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
 - IVisualTreeService3.RemoveDictionaryItem
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IVisualTreeService3::RemoveDictionaryItem


## -description


	Removes an item from a <a href="https://msdn.microsoft.com/cb82a1f5-ebcf-4ffd-842b-78313e5eff9c">ResourceDictionary</a>, and re-resolves all elements in the tree that reference a resource with the specified key.


## -parameters




### -param dictionaryHandle [in]

The dictionary to remove the resource from.


### -param resourceKey [in]

The key of the resource to remove.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Any invalid resource references will result in the value being cleared, and <a href="https://msdn.microsoft.com/F1C11F32-9524-49D6-89DD-C89E4A81720A">IVisualTreeServiceCallback2</a>  will be notified.




## -see-also




<a href="https://msdn.microsoft.com/20AD2DC4-388E-458E-AA44-8B2F3464FD6C">IVisualTreeService3</a>
 

 

