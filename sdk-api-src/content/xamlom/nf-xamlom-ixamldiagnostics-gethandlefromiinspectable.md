---
UID: NF:xamlom.IXamlDiagnostics.GetHandleFromIInspectable
title: IXamlDiagnostics::GetHandleFromIInspectable (xamlom.h)
description: Gets an InstanceHandle representation of an IInspectable.
helpviewer_keywords: ["GetHandleFromIInspectable","GetHandleFromIInspectable method","GetHandleFromIInspectable method","IXamlDiagnostics interface","IXamlDiagnostics interface","GetHandleFromIInspectable method","IXamlDiagnostics.GetHandleFromIInspectable","IXamlDiagnostics::GetHandleFromIInspectable","xaml_diagnostics.ixamldiagnostics_gethandlefromiinspectable","xamlom/IXamlDiagnostics::GetHandleFromIInspectable"]
old-location: xaml_diagnostics\ixamldiagnostics_gethandlefromiinspectable.htm
tech.root: xaml_diagnostics
ms.assetid: 334497D9-11ED-4002-AEAB-0454EB62E53C
ms.date: 12/05/2018
ms.keywords: GetHandleFromIInspectable, GetHandleFromIInspectable method, GetHandleFromIInspectable method,IXamlDiagnostics interface, IXamlDiagnostics interface,GetHandleFromIInspectable method, IXamlDiagnostics.GetHandleFromIInspectable, IXamlDiagnostics::GetHandleFromIInspectable, xaml_diagnostics.ixamldiagnostics_gethandlefromiinspectable, xamlom/IXamlDiagnostics::GetHandleFromIInspectable
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
 - IXamlDiagnostics::GetHandleFromIInspectable
 - xamlom/IXamlDiagnostics::GetHandleFromIInspectable
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
 - IXamlDiagnostics.GetHandleFromIInspectable
---

# IXamlDiagnostics::GetHandleFromIInspectable


## -description

Gets an <b>InstanceHandle</b> representation of an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>.

## -parameters

### -param pInstance [in]

An instance of the object as an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>.

### -param pHandle [out, retval]

A handle to the object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>