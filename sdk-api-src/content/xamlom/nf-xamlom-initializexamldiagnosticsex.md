---
UID: NF:xamlom.InitializeXamlDiagnosticsEx
title: InitializeXamlDiagnosticsEx function (xamlom.h)
description: Initializes a Xaml Diagnostics session. This is the entry point for any debugging tool using the XAML Diagnostic APIs.
helpviewer_keywords: ["InitializeXamlDiagnosticsEx","InitializeXamlDiagnosticsEx function","xaml_diagnostics.initializexamldiagnosticsex","xamlom/InitializeXamlDiagnosticsEx"]
old-location: xaml_diagnostics\initializexamldiagnosticsex.htm
tech.root: xaml_diagnostics
ms.assetid: CFBCF6EC-5E42-4992-B046-B4F436A9BF04
ms.date: 12/05/2018
ms.keywords: InitializeXamlDiagnosticsEx, InitializeXamlDiagnosticsEx function, xaml_diagnostics.initializexamldiagnosticsex, xamlom/InitializeXamlDiagnosticsEx
req.header: xamlom.h
req.include-header: Windows.UI.Xaml.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1703 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: Windows.UI.Xaml.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - InitializeXamlDiagnosticsEx
 - xamlom/InitializeXamlDiagnosticsEx
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - InitializeXamlDiagnosticsEx
---

# InitializeXamlDiagnosticsEx function


## -description

Initializes a Xaml Diagnostics session. This is the entry point for any debugging tool using the XAML Diagnostic APIs.

## -parameters

### -param endPointName [in]

The end point name for Visual Diagnostics.

### -param pid [in]

The pid of the process to connect to.

### -param wszDllXamlDiagnostics [in]

The path to XamlDiagnostics.dll.

### -param wszTAPDllName [in]

The name of the DLL to be injected in the process.

### -param tapClsid [in]

The COM CLSID of an object implementing IObjectWithSite, to be created from the DLL to be injected in the process. The site object will implement IXamlDiagnostics.

### -param wszInitializationData [in]

Initialization data for Xaml Diagnostics.

