---
UID: NF:xamlom.IVisualTreeService2.ReplaceResource
title: IVisualTreeService2::ReplaceResource (xamlom.h)
description: Replaces an existing resource with a new one of the same type.
helpviewer_keywords: ["IVisualTreeService2 interface","ReplaceResource method","IVisualTreeService2.ReplaceResource","IVisualTreeService2::ReplaceResource","ReplaceResource","ReplaceResource method","ReplaceResource method","IVisualTreeService2 interface","xaml_diagnostics.ivisualtreeservice2_replaceresource","xamlom/IVisualTreeService2::ReplaceResource"]
old-location: xaml_diagnostics\ivisualtreeservice2_replaceresource.htm
tech.root: xaml_diagnostics
ms.assetid: DD2066B0-C91E-4299-AFD3-13E74E75E94B
ms.date: 12/05/2018
ms.keywords: IVisualTreeService2 interface,ReplaceResource method, IVisualTreeService2.ReplaceResource, IVisualTreeService2::ReplaceResource, ReplaceResource, ReplaceResource method, ReplaceResource method,IVisualTreeService2 interface, xaml_diagnostics.ivisualtreeservice2_replaceresource, xamlom/IVisualTreeService2::ReplaceResource
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - IVisualTreeService2::ReplaceResource
 - xamlom/IVisualTreeService2::ReplaceResource
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
 - IVisualTreeService2.ReplaceResource
---

# IVisualTreeService2::ReplaceResource


## -description

Replaces an existing resource with a new one of the same type.

## -parameters

### -param resourceDictionary [in]

The dictionary that contains the resource to replace.

### -param key [in]

The key of the resource to replace.

### -param newValue [in]

The value to replace the resource with.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice2">IVisualTreeService2</a>



<a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice3-adddictionaryitem">IVisualTreeService3::AddDictionaryItem</a>



<a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice3-removedictionaryitem">IVisualTreeService3::RemoveDictionaryItem</a>