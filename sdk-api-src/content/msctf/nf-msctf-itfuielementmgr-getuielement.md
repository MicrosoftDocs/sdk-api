---
UID: NF:msctf.ITfUIElementMgr.GetUIElement
title: ITfUIElementMgr::GetUIElement
author: windows-sdk-content
description: The ITfUIElementMgr::GetUIElement method gets the ITfUIElement interface of the element id.
old-location: tsf\itfuielementmgr_getuielement.htm
tech.root: TSF
ms.assetid: e3a2a7ae-1ca2-4c1e-83af-207821966147
ms.author: windowssdkdev
ms.date: 08/30/2018
ms.keywords: GetUIElement, GetUIElement method [Text Services Framework], GetUIElement method [Text Services Framework],ITfUIElementMgr interface, ITfUIElementMgr interface [Text Services Framework],GetUIElement method, ITfUIElementMgr.GetUIElement, ITfUIElementMgr::GetUIElement, msctf/ITfUIElementMgr::GetUIElement, tsf.itfuielementmgr_getuielement
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfUIElementMgr.GetUIElement
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfUIElementMgr::GetUIElement


## -description


The <b>ITfUIElementMgr::GetUIElement</b> method gets the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface of the element id.


## -parameters




### -param dwUIELementId

TBD


### -param ppElement [out]

[out] A pointer to receive <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface.


#### - dwUIElementId [in]

[in] The element id to get the <a href="https://msdn.microsoft.com/651c3ca1-5e5b-4978-80d2-2183bd158610">ITfUIElement</a> interface.


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
</table>
 



