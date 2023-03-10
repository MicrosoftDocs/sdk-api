---
UID: NN:inputpaneinterop.IInputPaneInterop
title: IInputPaneInterop (inputpaneinterop.h)
description: Enables access to the members of the InputPane class in a desktop app.
helpviewer_keywords: ["IInputPaneInterop","IInputPaneInterop interface [Windows Runtime]","IInputPaneInterop interface [Windows Runtime]","described","inputpaneinterop/IInputPaneInterop","winrt.iinputpaneinterop"]
old-location: winrt\iinputpaneinterop.htm
tech.root: WinRT
ms.assetid: DAE4705C-B786-44D4-8B03-1523EFC4C190
ms.date: 12/05/2018
ms.keywords: IInputPaneInterop, IInputPaneInterop interface [Windows Runtime], IInputPaneInterop interface [Windows Runtime],described, inputpaneinterop/IInputPaneInterop, winrt.iinputpaneinterop
req.header: inputpaneinterop.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1607 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: InputPaneInterop.idl
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
 - IInputPaneInterop
 - inputpaneinterop/IInputPaneInterop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - inputpaneinterop.h
api_name:
 - IInputPaneInterop
---

# IInputPaneInterop interface


## -description

Enables access to the members of the <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> class in a desktop app.

## -inheritance

The <b>IInputPaneInterop</b> interface inherits from <a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IInputPaneInterop</b> also has these types of members:

## -remarks

You can obtain an instance of the <b>IInputPaneInterop</b> interface by calling the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method on the activation factory instance for the <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> class.

 



For an example that uses the <b>IInputPaneInterop</b> interface, see the <a href="https://github.com/Microsoft/WPF-Samples/tree/master/Input and Commands/TouchKeyboard/TouchKeyboardNotifier">touch keyboard notification WPF sample</a>.

The following example shows the definition of the IInputPaneInterop interface.


``` syntax
[
    uuid(75CF2C57-9195-4931-8332-F0B409E916AF),
]
interface IInputPaneInterop : IInspectable
{
    // Creates an instance of InputPane initialized with the window handle.
    HRESULT GetForWindow([in] HWND appWindow, [in] REFIID riid,
        [out, retval, iid_is(riid)] void** inputPane);
}

```

For store apps, use the <a href="/uwp/api/windows.ui.viewmanagement.inputpane.getforcurrentview">InputPane.GetForCurrentView</a> method to get an <a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object.

## -see-also

<a href="/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a>



<a href="/dotnet/api/system.runtime.interopservices.windowsruntime.windowsruntimemarshal.getactivationfactory#System_Runtime_InteropServices_WindowsRuntime_WindowsRuntimeMarshal_GetActivationFactory_System_Type_">WindowsRuntimeMarshal.GetActivationFactory</a>
