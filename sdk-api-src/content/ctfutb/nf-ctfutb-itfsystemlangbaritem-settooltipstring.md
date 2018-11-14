---
UID: NF:ctfutb.ITfSystemLangBarItem.SetTooltipString
title: ITfSystemLangBarItem::SetTooltipString
author: windows-sdk-content
description: ITfSystemLangBarItem::SetTooltipString method
old-location: tsf\itfsystemlangbaritem_settooltipstring.htm
tech.root: TSF
ms.assetid: 6917fcd1-acce-4e5d-b04f-ee8ea69e71b4
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: ITfSystemLangBarItem interface [Text Services Framework],SetTooltipString method, ITfSystemLangBarItem.SetTooltipString, ITfSystemLangBarItem::SetTooltipString, SetTooltipString, SetTooltipString method [Text Services Framework], SetTooltipString method [Text Services Framework],ITfSystemLangBarItem interface, _tsf_itfsystemlangbaritem_settooltipstring_ref, ctfutb/ITfSystemLangBarItem::SetTooltipString, tsf.itfsystemlangbaritem_settooltipstring
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctfutb.idl
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
 - msctf.dll
api_name:
 - ITfSystemLangBarItem.SetTooltipString
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- ctfutb.h
: 
- ITfSystemLangBarItem.SetTooltipString
: 
---

# ITfSystemLangBarItem::SetTooltipString


## -description




## -parameters




### -param pchToolTip [in]

A string that appears as a tooltip.


### -param cch [in]

Size, in characters, of the string.


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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
The tooltip string for the system language bar menu cannot be modified.

</td>
</tr>
</table>
 




## -remarks



In response to this method, the system language bar menu should call <a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_TOOLTIP to force the language bar to obtain the new tooltip text.



