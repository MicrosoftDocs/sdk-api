---
UID: NF:msctf.ITfUIElementMgr.UpdateUIElement
title: ITfUIElementMgr::UpdateUIElement (msctf.h)
description: The ITfUIElementMgr::UpdateUIElement method is called by a text service when the UI element must be updated.
helpviewer_keywords: ["ITfUIElementMgr interface [Text Services Framework]","UpdateUIElement method","ITfUIElementMgr.UpdateUIElement","ITfUIElementMgr::UpdateUIElement","UpdateUIElement","UpdateUIElement method [Text Services Framework]","UpdateUIElement method [Text Services Framework]","ITfUIElementMgr interface","msctf/ITfUIElementMgr::UpdateUIElement","tsf.itfuielementmgr_updateuielement"]
old-location: tsf\itfuielementmgr_updateuielement.htm
tech.root: TSF
ms.assetid: c7df9abf-53a0-41a4-aac5-d90b9abfbeec
ms.date: 12/05/2018
ms.keywords: ITfUIElementMgr interface [Text Services Framework],UpdateUIElement method, ITfUIElementMgr.UpdateUIElement, ITfUIElementMgr::UpdateUIElement, UpdateUIElement, UpdateUIElement method [Text Services Framework], UpdateUIElement method [Text Services Framework],ITfUIElementMgr interface, msctf/ITfUIElementMgr::UpdateUIElement, tsf.itfuielementmgr_updateuielement
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
 - ITfUIElementMgr::UpdateUIElement
 - msctf/ITfUIElementMgr::UpdateUIElement
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
 - ITfUIElementMgr.UpdateUIElement
---

# ITfUIElementMgr::UpdateUIElement


## -description

The <b>ITfUIElementMgr::UpdateUIElement</b> method is called by a text service when the UI element must be updated.

## -parameters

### -param dwUIElementId [in]

[in] The element id to update the UI element.

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