---
UID: NF:xamlom.IXamlDiagnostics.HitTest
title: IXamlDiagnostics::HitTest (xamlom.h)
description: Gets all elements in the visual tree that fall within the specified rectangle.
helpviewer_keywords: ["HitTest","HitTest method","HitTest method","IXamlDiagnostics interface","IXamlDiagnostics interface","HitTest method","IXamlDiagnostics.HitTest","IXamlDiagnostics::HitTest","xaml_diagnostics.ixamldiagnostics_hittest","xamlom/IXamlDiagnostics::HitTest"]
old-location: xaml_diagnostics\ixamldiagnostics_hittest.htm
tech.root: xaml_diagnostics
ms.assetid: B7722F49-F477-4D24-9183-BC09A4A12730
ms.date: 12/05/2018
ms.keywords: HitTest, HitTest method, HitTest method,IXamlDiagnostics interface, IXamlDiagnostics interface,HitTest method, IXamlDiagnostics.HitTest, IXamlDiagnostics::HitTest, xaml_diagnostics.ixamldiagnostics_hittest, xamlom/IXamlDiagnostics::HitTest
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
 - IXamlDiagnostics::HitTest
 - xamlom/IXamlDiagnostics::HitTest
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
 - IXamlDiagnostics.HitTest
---

# IXamlDiagnostics::HitTest


## -description

Gets all elements in the visual tree that fall within the specified rectangle.

## -parameters

### -param rect [in]

The area to hit test.

### -param pCount [out]

The size of the array.

### -param ppInstanceHandles [out]

An array containing all elements.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method performs a hit test on the XAML visual tree and will return all elements
    regardless if they are enabled or invisible for hit testing. This method does not return collapsed elements as they do not participate in layout. <a href="/previous-versions/windows/desktop/api/xamlom/nf-xamlom-ivisualtreeservice-advisevisualtreechange">AdviseVisualTreeChange</a> must be called before this method. The element does not need to be fully enclosed in the 
    <i>rect</i> area to be returned.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>