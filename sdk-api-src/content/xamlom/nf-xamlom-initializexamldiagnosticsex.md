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

Example: `VisualDiagConnection1`

### -param pid [in]

The pid of the process to connect to.

### -param wszDllXamlDiagnostics [in]

The path to XamlDiagnostics.dll from the Windows SDK.

### -param wszTAPDllName [in]

The name of the tap DLL to be injected in the process.

The DLL must expose a COM class that implements the <a href="/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface.

### -param tapClsid [in]

The COM CLSID of the COM class that the tap DLL exposes.

### -param wszInitializationData [in]

Initialization data for Xaml Diagnostics.

<i>wszInitializationData</i> may be <b>NULL</b> if no additional initialization data is needed.

## -returns

Type: <b><a href="/windows/win32/com/structure-of-com-error-codes">HRESULT</a></b>

Returns <b>S_OK</b> on successful completion.

## -remarks

To start a XAML Diagnostics session with **InitializeXamlDiagnosticsEx**, create a tap DLL that exposes a COM class that implements the <a href="/windows/win32/api/ocidl/nn-ocidl-iobjectwithsite">IObjectWithSite</a> interface.
The dll will be injected into the target process if the call is successful.

The COM class that the tap DLL exposes is given an **XamlDiagnostics** object (that implements <a href="/windows/win32/api/xamlom/nn-xamlom-ixamldiagnostics">IXamlDiagnostics</a>, <a href="/windows/win32/api/xamlom/nn-xamlom-ivisualtreeservice">IVisualTreeService</a>, <a href="/windows/win32/api/xamlom/nn-xamlom-ivisualtreeservice2">IVisualTreeService2</a>, and <a href="/windows/win32/api/xamlom/nn-xamlom-ivisualtreeservice3">IVisualTreeService3</a>) via the <a href="/windows/win32/api/ocidl/nf-ocidl-iobjectwithsite-setsite">IObjectWithSite::SetSite</a> function.

**InitializeXamlDiagnosticsEx** isn't defined in any static library (.lib) yet but can be dynamically loaded from `Windows.UI.Xaml.dll`.

If calling **InitializeXamlDiagnosticsEx** does not initially return <b>S_OK</b>, subsequent calls may be successful.

If the target process is a low IL packaged AppContainer UWP app, you have to allow both DLLs (XamlDiagnostics.dll and the tap DLL) to be loaded and read by the process by right clicking them > Properties > Security > Edit > Add > type `ALL APPLICATION PACKAGES` in the text box > OK > check `Allow` for `Read & execute` and `Read` > OK > OK.


## Example

The following sample code illustrates the use of **InitializeXamlDiagnosticsEx**:

```cpp
typedef HRESULT (*InitializeXamlDiagnosticsExProto)(_In_ LPCWSTR endPointName, _In_ DWORD pid, _In_ LPCWSTR wszDllXamlDiagnostics, _In_ LPCWSTR wszTAPDllName, _In_ CLSID tapClsid, _In_ LPCWSTR wszInitializationData);

...

InitializeXamlDiagnosticsExProto InitializeXamlDiagnosticsExFn = (InitializeXamlDiagnosticsExProto)GetProcAddress(LoadLibraryW(L"Windows.UI.Xaml.dll"), "InitializeXamlDiagnosticsEx");
HRESULT hr = InitializeXamlDiagnosticsExFn(L"VisualDiagConnection1", 12345, L"C:\\Program Files (x86)\\Windows Kits\\10\\bin\\x64\\XamlDiagnostics\\xamldiagnostics.dll", L"MyXamlTap.dll", CLSID_myTAP, L"86c 874 9f0 410 478 47c 9ec a08 ");
```

