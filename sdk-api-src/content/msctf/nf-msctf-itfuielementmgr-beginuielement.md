---
UID: NF:msctf.ITfUIElementMgr.BeginUIElement
title: ITfUIElementMgr::BeginUIElement (msctf.h)
description: The ITfUIElementMgr::BeginUIElement method is called by a text service before showing UI. The value returned determines whether the UI for the text service should be shown or not.
helpviewer_keywords: ["BeginUIElement","BeginUIElement method [Text Services Framework]","BeginUIElement method [Text Services Framework]","ITfUIElementMgr interface","ITfUIElementMgr interface [Text Services Framework]","BeginUIElement method","ITfUIElementMgr.BeginUIElement","ITfUIElementMgr::BeginUIElement","msctf/ITfUIElementMgr::BeginUIElement","tsf.itfuielementmgr_beginuielement"]
old-location: tsf\itfuielementmgr_beginuielement.htm
tech.root: TSF
ms.assetid: 7c522920-8bd7-4385-b77d-34df26967179
ms.date: 12/05/2018
ms.keywords: BeginUIElement, BeginUIElement method [Text Services Framework], BeginUIElement method [Text Services Framework],ITfUIElementMgr interface, ITfUIElementMgr interface [Text Services Framework],BeginUIElement method, ITfUIElementMgr.BeginUIElement, ITfUIElementMgr::BeginUIElement, msctf/ITfUIElementMgr::BeginUIElement, tsf.itfuielementmgr_beginuielement
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
 - ITfUIElementMgr::BeginUIElement
 - msctf/ITfUIElementMgr::BeginUIElement
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
 - ITfUIElementMgr.BeginUIElement
---

# ITfUIElementMgr::BeginUIElement


## -description

The <b>ITfUIElementMgr::BeginUIElement</b> method is called by a text service before showing UI. The value returned determines whether the UI for the text service should be shown or not.

## -parameters

### -param pElement [in]

[in] A pointer to the <a href="/windows/desktop/api/msctf/nn-msctf-itfuielement">ITfUIElement</a> interface of the UIElement object.

### -param pbShow

[in, out] If false is returned, the application may draw the UI by itself and a text service does not show its own UI for this UI element.

### -param pdwUIElementId [out]

[out] A pointer to receive the ID of this UI element.

## -returns

This method can return one of these values.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
One or more parameters are invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
Recursion call of <a href="/windows/desktop/api/msctf/nn-msctf-itfuielementmgr">ITfUIElementMgr</a> interface happened.

</td>
</tr>
</table>