---
UID: NE:xamlom.VisualMutationType
title: VisualMutationType (xamlom.h)
description: Defines constants that specify whether the element was added to or removed from the live visual tree.
helpviewer_keywords: ["Add","Remove","VisualMutationType","VisualMutationType enumeration","xaml_diagnostics.visualmutationtype","xamlom/Add","xamlom/Remove","xamlom/VisualMutationType"]
old-location: xaml_diagnostics\visualmutationtype.htm
tech.root: xaml_diagnostics
ms.assetid: 9DAABF59-AC88-4B14-A7F1-470D4C0879FF
ms.date: 12/05/2018
ms.keywords: Add, Remove, VisualMutationType, VisualMutationType enumeration, xaml_diagnostics.visualmutationtype, xamlom/Add, xamlom/Remove, xamlom/VisualMutationType
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
req.typenames: VisualMutationType
req.redist: 
ms.custom: 19H1
f1_keywords:
 - VisualMutationType
 - xamlom/VisualMutationType
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - xamlom.h
api_name:
 - VisualMutationType
---

# VisualMutationType enumeration


## -description

Defines constants that specify whether the element was added to or removed from the live visual tree.

## -enum-fields

### -field Add:0

The child element was added to the visual tree of the parent element.

### -field Remove

The child element was removed from the visual tree of the parent element.

## -remarks

<b>VisualMutationType</b> is used by <a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ivisualtreeservicecallback">IVisualTreeServiceCallback</a> to indicate to the callback
whether the element is entering or leaving the live visual tree.
