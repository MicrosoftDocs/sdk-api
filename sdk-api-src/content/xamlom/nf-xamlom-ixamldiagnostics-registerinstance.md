---
UID: NF:xamlom.IXamlDiagnostics.RegisterInstance
title: IXamlDiagnostics::RegisterInstance (xamlom.h)
description: Adds an IInspectable to the XAML Diagnostics cache and returns the newly created InstanceHandle for the object.
helpviewer_keywords: ["IXamlDiagnostics interface","RegisterInstance method","IXamlDiagnostics.RegisterInstance","IXamlDiagnostics::RegisterInstance","RegisterInstance","RegisterInstance method","RegisterInstance method","IXamlDiagnostics interface","xaml_diagnostics.ixamldiagnostics_registerinstance","xamlom/IXamlDiagnostics::RegisterInstance"]
old-location: xaml_diagnostics\ixamldiagnostics_registerinstance.htm
tech.root: xaml_diagnostics
ms.assetid: B1BD13CE-6B20-45D0-83E2-AB7E15BDA6FC
ms.date: 12/05/2018
ms.keywords: IXamlDiagnostics interface,RegisterInstance method, IXamlDiagnostics.RegisterInstance, IXamlDiagnostics::RegisterInstance, RegisterInstance, RegisterInstance method, RegisterInstance method,IXamlDiagnostics interface, xaml_diagnostics.ixamldiagnostics_registerinstance, xamlom/IXamlDiagnostics::RegisterInstance
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
 - IXamlDiagnostics::RegisterInstance
 - xamlom/IXamlDiagnostics::RegisterInstance
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
 - IXamlDiagnostics.RegisterInstance
---

# IXamlDiagnostics::RegisterInstance


## -description

Adds an <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a> to the XAML Diagnostics cache and returns the newly created
    <b>InstanceHandle</b> for the object.

## -parameters

### -param pInstance [in]

An instance of the object.

### -param pInstanceHandle [out, retval]

A handle to the object.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/previous-versions/windows/desktop/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>