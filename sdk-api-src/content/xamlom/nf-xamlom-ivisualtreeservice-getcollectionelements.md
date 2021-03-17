---
UID: NF:xamlom.IVisualTreeService.GetCollectionElements
title: IVisualTreeService::GetCollectionElements (xamlom.h)
description: Gets the elements in a collection.
helpviewer_keywords: ["GetCollectionElements","GetCollectionElements method","GetCollectionElements method","IVisualTreeService interface","IVisualTreeService interface","GetCollectionElements method","IVisualTreeService.GetCollectionElements","IVisualTreeService::GetCollectionElements","xaml_diagnostics.ivisualtreeservice_getcollectionelements","xamlom/IVisualTreeService::GetCollectionElements"]
old-location: xaml_diagnostics\ivisualtreeservice_getcollectionelements.htm
tech.root: xaml_diagnostics
ms.assetid: 01A2694F-E9CF-4DD2-95EA-6CD5C72C65A8
ms.date: 12/05/2018
ms.keywords: GetCollectionElements, GetCollectionElements method, GetCollectionElements method,IVisualTreeService interface, IVisualTreeService interface,GetCollectionElements method, IVisualTreeService.GetCollectionElements, IVisualTreeService::GetCollectionElements, xaml_diagnostics.ivisualtreeservice_getcollectionelements, xamlom/IVisualTreeService::GetCollectionElements
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
 - IVisualTreeService::GetCollectionElements
 - xamlom/IVisualTreeService::GetCollectionElements
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
 - IVisualTreeService.GetCollectionElements
---

# IVisualTreeService::GetCollectionElements


## -description

Gets the elements in a collection.

## -parameters

### -param instanceHandle [in]

A handle to the collection object.

### -param startIndex [in]

The index in the  collection to start getting elements from.

### -param pElementCount [in, out]

The count of elements in the returned array.

### -param ppElementValues [out]

An array of elements returned from the collection.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For any collection method, the caller should query the properties of a known element
    and should only call this method if the property has <a href="/previous-versions/windows/desktop/api/xamlom/ne-xamlom-metadatabit">MetadataBit::IsValueCollection</a>set.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>