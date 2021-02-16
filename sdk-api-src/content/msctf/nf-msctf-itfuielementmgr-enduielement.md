---
UID: NF:msctf.ITfUIElementMgr.EndUIElement
title: ITfUIElementMgr::EndUIElement (msctf.h)
description: The ITfUIElementMgr::EndUIElement method is called by a text service when the element of UI is hidden.
helpviewer_keywords: ["EndUIElement","EndUIElement method [Text Services Framework]","EndUIElement method [Text Services Framework]","ITfUIElementMgr interface","ITfUIElementMgr interface [Text Services Framework]","EndUIElement method","ITfUIElementMgr.EndUIElement","ITfUIElementMgr::EndUIElement","msctf/ITfUIElementMgr::EndUIElement","tsf.itfuielementmgr_enduielement"]
old-location: tsf\itfuielementmgr_enduielement.htm
tech.root: TSF
ms.assetid: cec22994-c233-4f84-8237-749ef3cc8aff
ms.date: 12/05/2018
ms.keywords: EndUIElement, EndUIElement method [Text Services Framework], EndUIElement method [Text Services Framework],ITfUIElementMgr interface, ITfUIElementMgr interface [Text Services Framework],EndUIElement method, ITfUIElementMgr.EndUIElement, ITfUIElementMgr::EndUIElement, msctf/ITfUIElementMgr::EndUIElement, tsf.itfuielementmgr_enduielement
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
 - ITfUIElementMgr::EndUIElement
 - msctf/ITfUIElementMgr::EndUIElement
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
 - ITfUIElementMgr.EndUIElement
---

# ITfUIElementMgr::EndUIElement


## -description

The <b>ITfUIElementMgr::EndUIElement</b> method is called by a text service when the element of UI is hidden.

## -parameters

### -param dwUIElementId [in]

[in] The element id to hide the UI element.

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