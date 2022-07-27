---
UID: NF:xamlom.IXamlDiagnostics.GetDispatcher
title: IXamlDiagnostics::GetDispatcher (xamlom.h)
description: Gets the core dispatcher used to access elements on the UI thread.
helpviewer_keywords: ["GetDispatcher","GetDispatcher method","GetDispatcher method","IXamlDiagnostics interface","IXamlDiagnostics interface","GetDispatcher method","IXamlDiagnostics.GetDispatcher","IXamlDiagnostics::GetDispatcher","xaml_diagnostics.ixamldiagnostics_getdispatcher","xamlom/IXamlDiagnostics::GetDispatcher"]
old-location: xaml_diagnostics\ixamldiagnostics_getdispatcher.htm
tech.root: xaml_diagnostics
ms.assetid: 6C7605F7-BBD7-4FAD-AA35-A3DC18AA6FF3
ms.date: 12/05/2018
ms.keywords: GetDispatcher, GetDispatcher method, GetDispatcher method,IXamlDiagnostics interface, IXamlDiagnostics interface,GetDispatcher method, IXamlDiagnostics.GetDispatcher, IXamlDiagnostics::GetDispatcher, xaml_diagnostics.ixamldiagnostics_getdispatcher, xamlom/IXamlDiagnostics::GetDispatcher
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
 - IXamlDiagnostics::GetDispatcher
 - xamlom/IXamlDiagnostics::GetDispatcher
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
 - IXamlDiagnostics.GetDispatcher
---

# IXamlDiagnostics::GetDispatcher


## -description

Gets the core dispatcher used to access elements on the UI thread.

## -parameters

### -param ppDispatcher [out, retval]

The <a href="/uwp/api/windows.ui.core.coredispatcher">CoreDispatcher</a> instance used to access the UI thread.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>