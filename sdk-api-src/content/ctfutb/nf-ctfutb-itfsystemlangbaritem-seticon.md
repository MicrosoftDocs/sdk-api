---
UID: NF:ctfutb.ITfSystemLangBarItem.SetIcon
title: ITfSystemLangBarItem::SetIcon
author: windows-sdk-content
description: ITfSystemLangBarItem::SetIcon method
old-location: tsf\itfsystemlangbaritem_seticon.htm
old-project: TSF
ms.assetid: 6b83e2ec-ac2f-4fd6-8c7c-70b00baafdc1
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfSystemLangBarItem interface [Text Services Framework],SetIcon method, ITfSystemLangBarItem.SetIcon, ITfSystemLangBarItem::SetIcon, SetIcon, SetIcon method [Text Services Framework], SetIcon method [Text Services Framework],ITfSystemLangBarItem interface, _tsf_itfsystemlangbaritem_seticon_ref, ctfutb/ITfSystemLangBarItem::SetIcon, tsf.itfsystemlangbaritem_seticon
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: ctfutb.h
req.include-header: 
req.redist: TSF 1.0 on Windows 2000 Professional
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
tech.root: 
req.typenames: TfLBIClick
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfSystemLangBarItem.SetIcon
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemLangBarItem::SetIcon


## -description




## -parameters




### -param hIcon [in]

Contains the handle to the new icon.


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
The system language bar menu does not allow its icon to be modified.

</td>
</tr>
</table>
 




## -remarks



In response to this method, the system language bar menu should call <a href="https://msdn.microsoft.com/f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7">ITfLangBarItemSink::OnUpdate</a> with TF_LBI_ICON to force the language bar to obtain the new icon.



