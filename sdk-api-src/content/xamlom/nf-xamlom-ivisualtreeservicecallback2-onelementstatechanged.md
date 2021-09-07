---
UID: NF:xamlom.IVisualTreeServiceCallback2.OnElementStateChanged
title: IVisualTreeServiceCallback2::OnElementStateChanged (xamlom.h)
description: Communicates the state of an element in the visual tree when it changes.
helpviewer_keywords: ["IVisualTreeServiceCallback2 interface","OnElementStateChanged method","IVisualTreeServiceCallback2.OnElementStateChanged","IVisualTreeServiceCallback2::OnElementStateChanged","OnElementStateChanged","OnElementStateChanged method","OnElementStateChanged method","IVisualTreeServiceCallback2 interface","xaml_diagnostics.ivisualtreeservicecallback2_onelementstatechanged","xamlom/IVisualTreeServiceCallback2::OnElementStateChanged"]
old-location: xaml_diagnostics\ivisualtreeservicecallback2_onelementstatechanged.htm
tech.root: xaml_diagnostics
ms.assetid: A832FDC6-1485-432C-9A87-A3C94D0AF8CA
ms.date: 12/05/2018
ms.keywords: IVisualTreeServiceCallback2 interface,OnElementStateChanged method, IVisualTreeServiceCallback2.OnElementStateChanged, IVisualTreeServiceCallback2::OnElementStateChanged, OnElementStateChanged, OnElementStateChanged method, OnElementStateChanged method,IVisualTreeServiceCallback2 interface, xaml_diagnostics.ivisualtreeservicecallback2_onelementstatechanged, xamlom/IVisualTreeServiceCallback2::OnElementStateChanged
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
 - IVisualTreeServiceCallback2::OnElementStateChanged
 - xamlom/IVisualTreeServiceCallback2::OnElementStateChanged
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
 - IVisualTreeServiceCallback2.OnElementStateChanged
---

# IVisualTreeServiceCallback2::OnElementStateChanged


## -description

Communicates the state of an element in the visual tree when it changes.

## -parameters

### -param element

The XAML element in the visual tree.

### -param elementState

The state of the element.

### -param context

The path to the element.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

When any XAML diagnostics API results in a resource reference becoming invalid, this callback will be notified of the invalid reference. An instance handle will be given that corresponds to an element in the tree, and a string representation of the path to the invalid reference. The grammar for the syntax is: PropertyName:Full.Dotted.TypeName[Indexer] and paths can be separated with a forward slash ("/") to be chained together.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservicecallback2">IVisualTreeServiceCallback2</a>