---
UID: NF:xamlom.IXamlDiagnostics.GetIInspectableFromHandle
title: IXamlDiagnostics::GetIInspectableFromHandle (xamlom.h)
description: Gets the IInspectable from the XAML Diagnostics cache.
helpviewer_keywords: ["GetIInspectableFromHandle","GetIInspectableFromHandle method","GetIInspectableFromHandle method","IXamlDiagnostics interface","IXamlDiagnostics interface","GetIInspectableFromHandle method","IXamlDiagnostics.GetIInspectableFromHandle","IXamlDiagnostics::GetIInspectableFromHandle","xaml_diagnostics.ixamldiagnostics_getiinspectablefromhandle","xamlom/IXamlDiagnostics::GetIInspectableFromHandle"]
old-location: xaml_diagnostics\ixamldiagnostics_getiinspectablefromhandle.htm
tech.root: xaml_diagnostics
ms.assetid: F5BD99E0-CBAF-461C-9B4A-692604D4BAA9
ms.date: 12/05/2018
ms.keywords: GetIInspectableFromHandle, GetIInspectableFromHandle method, GetIInspectableFromHandle method,IXamlDiagnostics interface, IXamlDiagnostics interface,GetIInspectableFromHandle method, IXamlDiagnostics.GetIInspectableFromHandle, IXamlDiagnostics::GetIInspectableFromHandle, xaml_diagnostics.ixamldiagnostics_getiinspectablefromhandle, xamlom/IXamlDiagnostics::GetIInspectableFromHandle
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
 - IXamlDiagnostics::GetIInspectableFromHandle
 - xamlom/IXamlDiagnostics::GetIInspectableFromHandle
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
 - IXamlDiagnostics.GetIInspectableFromHandle
---

# IXamlDiagnostics::GetIInspectableFromHandle


## -description

Gets the <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> from the XAML Diagnostics
    cache.

## -parameters

### -param instanceHandle [in]

A handle to the object.

### -param ppInstance [out, retval]

The object as an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method will fail if XAML Diagnostics no longer has a reference to
    the element.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>