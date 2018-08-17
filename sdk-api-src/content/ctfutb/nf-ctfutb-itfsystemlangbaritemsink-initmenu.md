---
UID: NF:ctfutb.ITfSystemLangBarItemSink.InitMenu
title: ITfSystemLangBarItemSink::InitMenu
author: windows-sdk-content
description: ITfSystemLangBarItemSink::InitMenu method
old-location: tsf\itfsystemlangbaritemsink_initmenu.htm
old-project: TSF
ms.assetid: 6e8ba0ef-2f0a-4d67-95c1-06fee763bc14
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfSystemLangBarItemSink interface [Text Services Framework],InitMenu method, ITfSystemLangBarItemSink.InitMenu, ITfSystemLangBarItemSink::InitMenu, InitMenu, InitMenu method [Text Services Framework], InitMenu method [Text Services Framework],ITfSystemLangBarItemSink interface, _tsf_itfsystemlangbaritemsink_initmenu_ref, ctfutb/ITfSystemLangBarItemSink::InitMenu, tsf.itfsystemlangbaritemsink_initmenu
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
 - Msctf.dll
api_name:
 - ITfSystemLangBarItemSink.InitMenu
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfSystemLangBarItemSink::InitMenu


## -description




## -parameters




### -param pMenu [in]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms628780(v=VS.85).aspx">ITfMenu</a> interface that the system language bar item uses to add items to the system language bar menu.


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
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/303115e1-8d52-4a0a-b05e-b5c92b8b3e2a">ITfMenu
      </a>



<a href="https://msdn.microsoft.com/en-us/library/ms628957(v=VS.85).aspx">ITfSystemLangBarItemSink</a>
 

 

