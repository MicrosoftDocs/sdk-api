---
UID: NF:ctfutb.ITfLangBarItemMgr.AdviseItemsSink
title: ITfLangBarItemMgr::AdviseItemsSink
author: windows-sdk-content
description: ITfLangBarItemMgr::AdviseItemsSink method
old-location: tsf\itflangbaritemmgr_adviseitemssink.htm
old-project: TSF
ms.assetid: c0a3e86b-487b-410a-8bba-c2b5126126d2
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: AdviseItemsSink, AdviseItemsSink method [Text Services Framework], AdviseItemsSink method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],AdviseItemsSink method, ITfLangBarItemMgr.AdviseItemsSink, ITfLangBarItemMgr::AdviseItemsSink, _tsf_itflangbaritemmgr_adviseitemssink_ref, ctfutb/ITfLangBarItemMgr::AdviseItemsSink, tsf.itflangbaritemmgr_adviseitemssink
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
req.typenames: TfLBIClick
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	msctf.dll
api_name:
-	ITfLangBarItemMgr.AdviseItemsSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemMgr::AdviseItemsSink


## -description




## -parameters




### -param ulCount [in]

Contains the number of advise sinks to install.


### -param ppunk [in]

Pointer to an array of <a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink</a> objects to install. This array must be at least <i>ulCount</i> elements in length.


### -param pguidItem [in]

Pointer to an array of <b>GUID</b>s that identify the items to install the advise sinks for. These are the item <b>GUID</b>s that the item supplies in <a href="https://msdn.microsoft.com/b32e433a-c0d6-418e-bf11-2291c85373c2">ITfLangBarItem::GetInfo</a>. This array must be at least <i>ulCount</i> elements in length.


### -param pdwCookie [out]

Pointer to an array of <b>DWORD</b>s that receive the cooresponding advise sink identification cookies. These cookies identify the advise sinks when they are removed with the <a href="https://msdn.microsoft.com/20a0f69b-950e-4ad7-9357-74f0b4a75c6b">ITfLangBarItemMgr::UnadviseItemSink</a> or <a href="https://msdn.microsoft.com/e15fb870-bedc-412d-9561-4db6c0515799">ITfLangBarItemMgr::UnadviseItemsSink</a> method. This array must be at least <i>ulCount</i> elements in length.


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




<a href="https://msdn.microsoft.com/b32e433a-c0d6-418e-bf11-2291c85373c2">ITfLangBarItem::GetInfo</a>



<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/20a0f69b-950e-4ad7-9357-74f0b4a75c6b">ITfLangBarItemMgr::UnadviseItemSink
      </a>



<b>
        ITfLangBarItemMgr::UnadviseItemsSink
      </b>



<a href="https://msdn.microsoft.com/1734a011-1ee8-4afd-ace8-334eeaf14518">ITfLangBarItemSink</a>
 

 

