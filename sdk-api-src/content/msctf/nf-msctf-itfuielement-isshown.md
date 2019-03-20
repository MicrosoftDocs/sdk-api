---
UID: NF:msctf.ITfUIElement.IsShown
title: ITfUIElement::IsShown (msctf.h)
author: windows-sdk-content
description: The ITfUIElement::IsShown method returns true if the UI is currently shown by a text service; otherwise false.
old-location: tsf\itfuielement_isshown.htm
tech.root: TSF
ms.assetid: 84253cbe-a30e-4def-b268-0f5f1b7d54dc
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: ITfUIElement interface [Text Services Framework],IsShown method, ITfUIElement.IsShown, ITfUIElement::IsShown, IsShown, IsShown method [Text Services Framework], IsShown method [Text Services Framework],ITfUIElement interface, msctf/ITfUIElement::IsShown, tsf.itfuielement_isshown
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
 - ITfUIElement.IsShown
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfUIElement::IsShown


## -description


The <b>ITfUIElement::IsShown</b> method returns true if the UI is currently shown by a text service; otherwise false.


## -parameters




### -param pbShow [out]

[out] A pointer to bool of the current show status of the original UI of this element.


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
 



