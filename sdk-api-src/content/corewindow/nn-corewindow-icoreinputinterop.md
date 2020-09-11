---
UID: NN:corewindow.ICoreInputInterop
title: ICoreInputInterop (corewindow.h)
description: Enables an input source on a Windows application's core input object.
helpviewer_keywords: ["ICoreInputInterop","ICoreInputInterop interface [Windows Runtime]","ICoreInputInterop interface [Windows Runtime]","described","corewindow/ICoreInputInterop","winrt.icoreinputinterop"]
old-location: winrt\icoreinputinterop.htm
tech.root: WinRT
ms.assetid: F7BA7EFB-D9DC-4FF2-97A4-C4818BCBD599
ms.date: 12/05/2018
ms.keywords: ICoreInputInterop, ICoreInputInterop interface [Windows Runtime], ICoreInputInterop interface [Windows Runtime],described, corewindow/ICoreInputInterop, winrt.icoreinputinterop
req.header: corewindow.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ICoreInputInterop
 - corewindow/ICoreInputInterop
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - corewindow.h
api_name:
 - ICoreInputInterop
---

# ICoreInputInterop interface


## -description

Enables an input source on a Windows application's core input object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreInputInterop</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICoreInputInterop</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>ICoreInputInterop</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/corewindow/nf-corewindow-icoreinputinterop-setinputsource">SetInputSource</a>
</td>
<td align="left" width="63%">
Sets the input source for an app's <a href="https://docs.microsoft.com/dotnet/api/microsoft.toolkit.win32.ui.controls.interop.winrt.coreindependentinputsource?view=win-comm-toolkit-dotnet-stable">CoreIndependentInputSource</a> or <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.corecomponentinputsource">CoreComponentInputSource</a>.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ICoreInputInterop</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://docs.microsoft.com/windows/desktop/api/corewindow/nf-corewindow-icoreinputinterop-put_messagehandled">MessageHandled</a>

</td>
<td align="left" width="10%">
Write-only

</td>
<td align="left" width="63%">
Sets whether or not the message to the <a href="https://msdn.microsoft.com/60b1c8c6-c136-4c4c-8e46-69a792d58ed0">CoreWindow</a> has been handled.

</td>
</tr>
</table>

## -remarks

The <a href="https://docs.microsoft.com/dotnet/api/microsoft.toolkit.win32.ui.controls.interop.winrt.coreindependentinputsource?view=win-comm-toolkit-dotnet-stable">CoreIndependentInputSource</a> or <a href="https://docs.microsoft.com/uwp/api/windows.ui.core.corecomponentinputsource">CoreComponentInputSource</a> object defines the basic keyboard and pointer input events  for a Windows Store app.

## -see-also

<a href="https://docs.microsoft.com/uwp/api/windows.ui.core.corecomponentinputsource">CoreComponentInputSource</a>

<a href="https://docs.microsoft.com/dotnet/api/microsoft.toolkit.win32.ui.controls.interop.winrt.coreindependentinputsource?view=win-comm-toolkit-dotnet-stable">CoreIndependentInputSource</a>

