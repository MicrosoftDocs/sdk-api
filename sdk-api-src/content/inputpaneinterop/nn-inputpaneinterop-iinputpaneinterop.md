---
UID: NN:inputpaneinterop.IInputPaneInterop
title: IInputPaneInterop (inputpaneinterop.h)
description: Enables access to the members of the InputPane class in a desktop app.
old-location: winrt\iinputpaneinterop.htm
tech.root: WinRT
ms.assetid: DAE4705C-B786-44D4-8B03-1523EFC4C190
ms.date: 12/05/2018
ms.keywords: IInputPaneInterop, IInputPaneInterop interface [Windows Runtime], IInputPaneInterop interface [Windows Runtime],described, inputpaneinterop/IInputPaneInterop, winrt.iinputpaneinterop
f1_keywords:
- inputpaneinterop/IInputPaneInterop
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- inputpaneinterop.h
api_name:
- IInputPaneInterop
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IInputPaneInterop interface


## -description


Enables access to the members of the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> class in a desktop app.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputPaneInterop</b> interface inherits from <a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>. <b>IInputPaneInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IInputPaneInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inputpaneinterop/nf-inputpaneinterop-iinputpaneinterop-getforwindow">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets an instance of an <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-getiids">GetIids</a>
</td>
<td align="left" width="63%">
Gets the interfaces that are implemented by the current Windows Runtime class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-getruntimeclassname">GetRuntimeClassName</a>
</td>
<td align="left" width="63%">
Gets the fully qualified name of the current Windows Runtime object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nf-inspectable-iinspectable-gettrustlevel">GetTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current Windows Runtime object.

</td>
</tr>
</table> 


## -remarks



You can obtain an instance of the <b>IInputPaneInterop</b> interface by calling the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">IUnknown::QueryInterface</a> method on the activation factory instance for the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> class.

 



For an example that uses the <b>IInputPaneInterop</b> interface, see the <a href="https://github.com/Microsoft/WPF-Samples/tree/master/Input and Commands/TouchKeyboard/TouchKeyboardNotifier">touch keyboard notification WPF sample</a>.

The following example shows the definition of the IInputPaneInterop interface.

<pre class="syntax" xml:space="preserve"><code>[
    uuid(75CF2C57-9195-4931-8332-F0B409E916AF),
]
interface IInputPaneInterop : IInspectable
{
    // Creates an instance of InputPane initialized with the window handle.
    HRESULT GetForWindow([in] HWND appWindow, [in] REFIID riid,
        [out, retval, iid_is(riid)] void** inputPane);
}
</code></pre>
For store apps, use the <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane.getforcurrentview">InputPane.GetForCurrentView</a> method to get an <a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a> object.





## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/inspectable/nn-inspectable-iinspectable">IInspectable</a>



<a href="https://docs.microsoft.com/en-us/uwp/api/windows.ui.viewmanagement.inputpane">InputPane</a>



<a href="https://docs.microsoft.com/dotnet/api/system.runtime.interopservices.windowsruntime.windowsruntimemarshal.getactivationfactory?redirectedfrom=MSDN#System_Runtime_InteropServices_WindowsRuntime_WindowsRuntimeMarshal_GetActivationFactory_System_Type_">WindowsRuntimeMarshal.GetActivationFactory</a>
 

 

