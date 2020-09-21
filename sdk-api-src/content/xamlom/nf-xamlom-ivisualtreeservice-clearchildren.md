---
UID: NF:xamlom.IVisualTreeService.ClearChildren
title: IVisualTreeService::ClearChildren (xamlom.h)
description: Clears all child elements from the parent collection.
helpviewer_keywords: ["ClearChildren","ClearChildren method","ClearChildren method","IVisualTreeService interface","IVisualTreeService interface","ClearChildren method","IVisualTreeService.ClearChildren","IVisualTreeService::ClearChildren","xaml_diagnostics.ivisualtreeservice_clearchildren","xamlom/IVisualTreeService::ClearChildren"]
old-location: xaml_diagnostics\ivisualtreeservice_clearchildren.htm
tech.root: xaml_diagnostics
ms.assetid: E32B07F5-BB62-435A-A869-36A0E93915D9
ms.date: 12/05/2018
ms.keywords: ClearChildren, ClearChildren method, ClearChildren method,IVisualTreeService interface, IVisualTreeService interface,ClearChildren method, IVisualTreeService.ClearChildren, IVisualTreeService::ClearChildren, xaml_diagnostics.ivisualtreeservice_clearchildren, xamlom/IVisualTreeService::ClearChildren
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
 - IVisualTreeService::ClearChildren
 - xamlom/IVisualTreeService::ClearChildren
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
 - IVisualTreeService.ClearChildren
---

# IVisualTreeService::ClearChildren


## -description

Clears all child elements from the parent collection.

## -parameters

### -param parent [in]

A handle to the collection object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit::IsValueCollection</a>set.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>