---
UID: NN:inputpaneinterop.IInputPaneInterop
title: IInputPaneInterop
author: windows-sdk-content
description: Enables access to the members of the InputPane class in a desktop app.
old-location: winrt\iinputpaneinterop.htm
tech.root: WinRT
ms.assetid: DAE4705C-B786-44D4-8B03-1523EFC4C190
ms.author: windowssdkdev
ms.date: 10/26/2018
ms.keywords: IInputPaneInterop, IInputPaneInterop interface [Windows Runtime], IInputPaneInterop interface [Windows Runtime],described, inputpaneinterop/IInputPaneInterop, winrt.iinputpaneinterop
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IInputPaneInterop interface


## -description


Enables access to the members of the <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> class in a desktop app.  


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IInputPaneInterop</b> interface inherits from <a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>. <b>IInputPaneInterop</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/98A591F8-B85C-4400-9BA6-1B8F422C067B">GetForWindow</a>
</td>
<td align="left" width="63%">
Gets an instance of an <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object for the specified window.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/560094E6-3ED2-4BF3-85C7-07736ECBACC8">GetIids</a>
</td>
<td align="left" width="63%">
Gets the interfaces that are implemented by the current Windows Runtime class.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E0A0B56D-E676-46FD-873D-11309102DFFD">GetRuntimeClassName</a>
</td>
<td align="left" width="63%">
Gets the fully qualified name of the current Windows Runtime object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/E7E8AFD1-A8B7-4023-9F8B-573E0D2622F6">GetTrustLevel</a>
</td>
<td align="left" width="63%">
Gets the trust level of the current Windows Runtime object.

</td>
</tr>
</table> 


## -remarks



You can obtain an instance of the <b>IInputPaneInterop</b> interface by calling the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface</a> method on the activation factory instance for the <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> class.

 



For an example that uses the <b>IInputPaneInterop</b> interface, see the <a href="https://go.microsoft.com/fwlink/p/?linkid=837837">touch keyboard notification WPF sample</a>.

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
For store apps, use the <a href="https://msdn.microsoft.com/7eda6937-7ee7-430a-b9f8-656fa7404873">InputPane.GetForCurrentView</a> method to get an <a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a> object.





## -see-also




<a href="https://msdn.microsoft.com/0657E51F-D4C0-46C6-927D-B01E54B6846C">IInspectable</a>



<a href="https://msdn.microsoft.com/d0a72cb8-a0b2-4c32-9719-79a9f6b7b96c">InputPane</a>



<a href="https://msdn.microsoft.com/library/Hh551827(v=VS.105).aspx">WindowsRuntimeMarshal.GetActivationFactory</a>
 

 

