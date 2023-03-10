---
UID: NF:xamlom.IVisualTreeServiceCallback.OnVisualTreeChange
title: IVisualTreeServiceCallback::OnVisualTreeChange (xamlom.h)
description: Communicates the state of the visual tree when it changes.
helpviewer_keywords: ["IVisualTreeServiceCallback interface","OnVisualTreeChange method","IVisualTreeServiceCallback.OnVisualTreeChange","IVisualTreeServiceCallback::OnVisualTreeChange","OnVisualTreeChange","OnVisualTreeChange method","OnVisualTreeChange method","IVisualTreeServiceCallback interface","xaml_diagnostics.ivisualtreeservicecallback_onvisualtreechange","xamlom/IVisualTreeServiceCallback::OnVisualTreeChange"]
old-location: xaml_diagnostics\ivisualtreeservicecallback_onvisualtreechange.htm
tech.root: xaml_diagnostics
ms.assetid: 91D128E7-ECCA-426D-A6D6-773672302C6C
ms.date: 12/05/2018
ms.keywords: IVisualTreeServiceCallback interface,OnVisualTreeChange method, IVisualTreeServiceCallback.OnVisualTreeChange, IVisualTreeServiceCallback::OnVisualTreeChange, OnVisualTreeChange, OnVisualTreeChange method, OnVisualTreeChange method,IVisualTreeServiceCallback interface, xaml_diagnostics.ivisualtreeservicecallback_onvisualtreechange, xamlom/IVisualTreeServiceCallback::OnVisualTreeChange
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
 - IVisualTreeServiceCallback::OnVisualTreeChange
 - xamlom/IVisualTreeServiceCallback::OnVisualTreeChange
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
 - IVisualTreeServiceCallback.OnVisualTreeChange
---

# IVisualTreeServiceCallback::OnVisualTreeChange


## -description

Communicates the state of the visual tree when it changes.

## -parameters

### -param relation [in]

The association of  a parent object with a child object.

### -param element [in]

The XAML element in the visual tree.

### -param mutationType [in]

A value that indicates whether the change was an add or remove.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservicecallback">IVisualTreeServiceCallback</a>