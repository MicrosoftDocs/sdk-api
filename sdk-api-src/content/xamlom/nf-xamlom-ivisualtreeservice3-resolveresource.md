---
UID: NF:xamlom.IVisualTreeService3.ResolveResource
title: IVisualTreeService3::ResolveResource (xamlom.h)
description: Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.
helpviewer_keywords: ["IVisualTreeService3 interface","ResolveResource method","IVisualTreeService3.ResolveResource","IVisualTreeService3::ResolveResource","ResolveResource","ResolveResource method","ResolveResource method","IVisualTreeService3 interface","xaml_diagnostics.ivisualtreeservice3_resolveresource","xamlom/IVisualTreeService3::ResolveResource"]
old-location: xaml_diagnostics\ivisualtreeservice3_resolveresource.htm
tech.root: xaml_diagnostics
ms.assetid: 7DDF1FD0-AD9B-4679-831D-CEDF6524181B
ms.date: 12/05/2018
ms.keywords: IVisualTreeService3 interface,ResolveResource method, IVisualTreeService3.ResolveResource, IVisualTreeService3::ResolveResource, ResolveResource, ResolveResource method, ResolveResource method,IVisualTreeService3 interface, xaml_diagnostics.ivisualtreeservice3_resolveresource, xamlom/IVisualTreeService3::ResolveResource
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
 - IVisualTreeService3::ResolveResource
 - xamlom/IVisualTreeService3::ResolveResource
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
 - IVisualTreeService3.ResolveResource
---

# IVisualTreeService3::ResolveResource


## -description

Resolves a resource for an element in the tree and applies the resource to the property provided by the specified property index.

## -parameters

### -param resourceContext [in]

The context of the resource.

### -param resourceName [in]

The name of the resource.

### -param resourceType [in]

The type of the resource.

### -param propertyIndex [in]

The index of the property to apply the resource to.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

 If no resource was found, or the resource type was invalid, <a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservicecallback2">IVisualTreeServiceCallback2</a>  will be notified.

Call <a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice3-getdictionaryitem">GetDictionaryItem</a> to get a <i>resourceContext</i> and give better resolution context for <b>ResolveResource</b>.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice3">IVisualTreeService3</a>