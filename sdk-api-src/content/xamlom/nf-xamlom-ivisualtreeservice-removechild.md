---
UID: NF:xamlom.IVisualTreeService.RemoveChild
title: IVisualTreeService::RemoveChild (xamlom.h)
description: Removes the child element from the specified index.
helpviewer_keywords: ["IVisualTreeService interface","RemoveChild method","IVisualTreeService.RemoveChild","IVisualTreeService::RemoveChild","RemoveChild","RemoveChild method","RemoveChild method","IVisualTreeService interface","xaml_diagnostics.ivisualtreeservice_removechild","xamlom/IVisualTreeService::RemoveChild"]
old-location: xaml_diagnostics\ivisualtreeservice_removechild.htm
tech.root: xaml_diagnostics
ms.assetid: 6D53C961-7E85-4275-8D65-454684606290
ms.date: 12/05/2018
ms.keywords: IVisualTreeService interface,RemoveChild method, IVisualTreeService.RemoveChild, IVisualTreeService::RemoveChild, RemoveChild, RemoveChild method, RemoveChild method,IVisualTreeService interface, xaml_diagnostics.ivisualtreeservice_removechild, xamlom/IVisualTreeService::RemoveChild
req.header: xamlom.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
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
 - IVisualTreeService::RemoveChild
 - xamlom/IVisualTreeService::RemoveChild
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
 - IVisualTreeService.RemoveChild
---

# IVisualTreeService::RemoveChild


## -description

Removes the child element from the specified index.

## -parameters

### -param parent [in]

A handle to the collection object.

### -param index [in]

Location in <i>parent</i> collection at which to remove the child element.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code. The method will fail if index is outside
    of the collection range.

## -remarks

For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit::IsValueCollection</a>set.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>