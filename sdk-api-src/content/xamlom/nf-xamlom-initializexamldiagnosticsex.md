---
UID: NF:xamlom.InitializeXamlDiagnosticsEx
title: InitializeXamlDiagnosticsEx function (xamlom.h)
author: windows-sdk-content
description: Initializes a Xaml Diagnostics session. This is the entry point for any debugging tool using the XAML Diagnostic APIs.
old-location: xaml_diagnostics\initializexamldiagnosticsex.htm
tech.root: xaml_diagnostics
ms.assetid: CFBCF6EC-5E42-4992-B046-B4F436A9BF04
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: InitializeXamlDiagnosticsEx, InitializeXamlDiagnosticsEx function, xaml_diagnostics.initializexamldiagnosticsex, xamlom/InitializeXamlDiagnosticsEx
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Windows.UI.Xaml.dll
api_name:
 - InitializeXamlDiagnosticsEx
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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

The COM CLSID of the DLL to be injected in the process.


### -param wszInitializationData [in]

Initialization data for Xaml Diagnostics.

