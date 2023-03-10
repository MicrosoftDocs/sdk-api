---
UID: NF:msctf.ITfUIElementSink.BeginUIElement
title: ITfUIElementSink::BeginUIElement (msctf.h)
description: The ITfUIElementSink::BeginUIElement method is called when the UIElement started. This sink can let the textservice to draw or not to draw the UI element.
helpviewer_keywords: ["BeginUIElement","BeginUIElement method [Text Services Framework]","BeginUIElement method [Text Services Framework]","ITfUIElementSink interface","ITfUIElementSink interface [Text Services Framework]","BeginUIElement method","ITfUIElementSink.BeginUIElement","ITfUIElementSink::BeginUIElement","msctf/ITfUIElementSink::BeginUIElement","tsf.itfuielementsink_beginuielement"]
old-location: tsf\itfuielementsink_beginuielement.htm
tech.root: TSF
ms.assetid: 068c6963-7d69-45b9-8f8b-7af358548a56
ms.date: 12/05/2018
ms.keywords: BeginUIElement, BeginUIElement method [Text Services Framework], BeginUIElement method [Text Services Framework],ITfUIElementSink interface, ITfUIElementSink interface [Text Services Framework],BeginUIElement method, ITfUIElementSink.BeginUIElement, ITfUIElementSink::BeginUIElement, msctf/ITfUIElementSink::BeginUIElement, tsf.itfuielementsink_beginuielement
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfUIElementSink::BeginUIElement
 - msctf/ITfUIElementSink::BeginUIElement
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfUIElementSink.BeginUIElement
---

# ITfUIElementSink::BeginUIElement


## -description

The <b>ITfUIElementSink::BeginUIElement</b> method is called when the UIElement started. This sink can let the textservice to draw or not to draw the UI element.

## -parameters

### -param dwUIElementId [in]

[in] Id of the UIElement that was started.

### -param pbShow

[in, out] Return <b>true</b> if the application does not draw the UIElement content and the text service draws its original UI content. Return <b>false</b> if the application draws the UIElement's content and stops the text service from drawing it. The application can get the <a href="/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a> interface by using <a href="/windows/desktop/api/msctf/nf-msctf-itfuielementmgr-getuielement">ITfUIElementMgr::GetUIElement</a> and it can evaluate if it can handle the UIElement by QI with <b>IID_ITfCandidateListUIElement</b> or with other UIElement interfaces. The application can always return <b>FALSE</b> if it is unknown or it cannot be handled. In this case, the text service will not show any extra UI on the screen. This is a good way for some full screen applications. Alternatively, the application can return <b>TRUE</b> to use TextService's UI on some particular or unknown UIs.

## -returns

The TSF manager ignores the return value of this method.

<table>
<tr>
<th>Value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_FAIL</b></dt>
</dl>
</td>
<td width="60%">
An unspecified error occurred.

</td>
</tr>
</table>