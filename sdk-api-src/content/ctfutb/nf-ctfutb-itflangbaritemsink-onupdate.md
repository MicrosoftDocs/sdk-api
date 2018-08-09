---
UID: NF:ctfutb.ITfLangBarItemSink.OnUpdate
title: ITfLangBarItemSink::OnUpdate
author: windows-sdk-content
description: ITfLangBarItemSink::OnUpdate method
old-location: tsf\itflangbaritemsink_onupdate.htm
old-project: TSF
ms.assetid: f4fbc301-efbe-4b43-b2bd-e1a7248ad2f7
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: ITfLangBarItemSink interface [Text Services Framework],OnUpdate method, ITfLangBarItemSink.OnUpdate, ITfLangBarItemSink::OnUpdate, OnUpdate, OnUpdate method [Text Services Framework], OnUpdate method [Text Services Framework],ITfLangBarItemSink interface, _tsf_itflangbaritemsink_onupdate_ref, ctfutb/ITfLangBarItemSink::OnUpdate, tsf.itflangbaritemsink_onupdate
ms.prod: windows
ms.technology: windows-sdk
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
 - ITfLangBarItemSink.OnUpdate
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemSink::OnUpdate


## -description




## -parameters




### -param dwFlags [in]

Contains a set of flags that indicate changes in the language bar item. This can be a combination of one or more of the <a href="https://msdn.microsoft.com/ed84012f-19ba-43b3-bbb5-7373ed174c33">TF_LBI_*</a> values.


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
 




## -remarks



A language bar item should call this method when the internal state of the item changes. TSF will update the language bar user interface appropriately.




## -see-also




<a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink</a>



<a href="https://msdn.microsoft.com/ed84012f-19ba-43b3-bbb5-7373ed174c33">TF_LBI_* Constants</a>
 

 

