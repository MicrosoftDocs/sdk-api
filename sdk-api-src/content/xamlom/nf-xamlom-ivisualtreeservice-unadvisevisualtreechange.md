---
UID: NF:xamlom.IVisualTreeService.UnadviseVisualTreeChange
title: IVisualTreeService::UnadviseVisualTreeChange (xamlom.h)
description: Stops listening for changes to the visual tree.
helpviewer_keywords: ["IVisualTreeService interface","UnadviseVisualTreeChange method","IVisualTreeService.UnadviseVisualTreeChange","IVisualTreeService::UnadviseVisualTreeChange","UnadviseVisualTreeChange","UnadviseVisualTreeChange method","UnadviseVisualTreeChange method","IVisualTreeService interface","xaml_diagnostics.ivisualtreeservice_unadvisevisualtreechange","xamlom/IVisualTreeService::UnadviseVisualTreeChange"]
old-location: xaml_diagnostics\ivisualtreeservice_unadvisevisualtreechange.htm
tech.root: xaml_diagnostics
ms.assetid: E77CBED8-F214-48AC-903E-F01B6EECA2ED
ms.date: 12/05/2018
ms.keywords: IVisualTreeService interface,UnadviseVisualTreeChange method, IVisualTreeService.UnadviseVisualTreeChange, IVisualTreeService::UnadviseVisualTreeChange, UnadviseVisualTreeChange, UnadviseVisualTreeChange method, UnadviseVisualTreeChange method,IVisualTreeService interface, xaml_diagnostics.ivisualtreeservice_unadvisevisualtreechange, xamlom/IVisualTreeService::UnadviseVisualTreeChange
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
 - IVisualTreeService::UnadviseVisualTreeChange
 - xamlom/IVisualTreeService::UnadviseVisualTreeChange
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
 - IVisualTreeService.UnadviseVisualTreeChange
---

# IVisualTreeService::UnadviseVisualTreeChange


## -description

Stops listening for changes to the visual tree.

## -parameters

### -param pCallback [in]

The callback to unregister for mutation events.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>UnadviseVisualTreeChange</b> should be called when the caller no longer wants to listen for
    mutation events.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>