---
UID: NF:xamlom.IXamlDiagnostics.GetUiLayer
title: IXamlDiagnostics::GetUiLayer (xamlom.h)
description: Gets the visual diagnostics root that can be used to draw on for highlighting elements in the tree.
helpviewer_keywords: ["GetUiLayer","GetUiLayer method","GetUiLayer method","IXamlDiagnostics interface","IXamlDiagnostics interface","GetUiLayer method","IXamlDiagnostics.GetUiLayer","IXamlDiagnostics::GetUiLayer","xaml_diagnostics.ixamldiagnostics_getuilayer","xamlom/IXamlDiagnostics::GetUiLayer"]
old-location: xaml_diagnostics\ixamldiagnostics_getuilayer.htm
tech.root: xaml_diagnostics
ms.assetid: BE45AF9E-0C2D-439B-A360-2B9AE9359AEE
ms.date: 12/05/2018
ms.keywords: GetUiLayer, GetUiLayer method, GetUiLayer method,IXamlDiagnostics interface, IXamlDiagnostics interface,GetUiLayer method, IXamlDiagnostics.GetUiLayer, IXamlDiagnostics::GetUiLayer, xaml_diagnostics.ixamldiagnostics_getuilayer, xamlom/IXamlDiagnostics::GetUiLayer
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
 - IXamlDiagnostics::GetUiLayer
 - xamlom/IXamlDiagnostics::GetUiLayer
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
 - IXamlDiagnostics.GetUiLayer
---

# IXamlDiagnostics::GetUiLayer


## -description

Gets the visual diagnostics root that can be used to draw
    on for highlighting elements in the tree.

## -parameters

### -param ppLayer [out, retval]

The visual diagnostics root.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>