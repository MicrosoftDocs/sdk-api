---
UID: NF:xamlom.IVisualTreeService.AddChild
title: IVisualTreeService::AddChild (xamlom.h)
description: Adds a child element to the collection at the specified index.
helpviewer_keywords: ["AddChild","AddChild method","AddChild method","IVisualTreeService interface","IVisualTreeService interface","AddChild method","IVisualTreeService.AddChild","IVisualTreeService::AddChild","xaml_diagnostics.ivisualtreeservice_addchild","xamlom/IVisualTreeService::AddChild"]
old-location: xaml_diagnostics\ivisualtreeservice_addchild.htm
tech.root: xaml_diagnostics
ms.assetid: 0F3BFACA-0B4C-4CC5-A48B-BD3921728612
ms.date: 12/05/2018
ms.keywords: AddChild, AddChild method, AddChild method,IVisualTreeService interface, IVisualTreeService interface,AddChild method, IVisualTreeService.AddChild, IVisualTreeService::AddChild, xaml_diagnostics.ivisualtreeservice_addchild, xamlom/IVisualTreeService::AddChild
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
 - IVisualTreeService::AddChild
 - xamlom/IVisualTreeService::AddChild
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
 - IVisualTreeService.AddChild
---

# IVisualTreeService::AddChild


## -description

Adds a child element to the collection at the specified index.

## -parameters

### -param parent [in]

A handle to the collection object.

### -param child [in]

A handle to the element to place into the collection. This can be newly created through <a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-createinstance">CreateInstance</a> or shared, such as <b>SolidColorBrush</b>.

### -param index [in]

Location in <i>parent</i> collection at which to insert <i>child</i> element.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit::IsValueCollection</a>set.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>