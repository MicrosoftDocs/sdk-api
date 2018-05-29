---
UID: NF:ctfutb.ITfLangBarItemMgr.UnadviseItemSink
title: ITfLangBarItemMgr::UnadviseItemSink
author: windows-sdk-content
description: ITfLangBarItemMgr::UnadviseItemSink method
old-location: tsf\itflangbaritemmgr_unadviseitemsink.htm
old-project: TSF
ms.assetid: 20a0f69b-950e-4ad7-9357-74f0b4a75c6b
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: ITfLangBarItemMgr interface [Text Services Framework],UnadviseItemSink method, ITfLangBarItemMgr.UnadviseItemSink, ITfLangBarItemMgr::UnadviseItemSink, UnadviseItemSink, UnadviseItemSink method [Text Services Framework], UnadviseItemSink method [Text Services Framework],ITfLangBarItemMgr interface, _tsf_itflangbaritemmgr_unadviseitemsink_ref, ctfutb/ITfLangBarItemMgr::UnadviseItemSink, tsf.itflangbaritemmgr_unadviseitemsink
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
-	ITfLangBarItemMgr.UnadviseItemSink
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemMgr::UnadviseItemSink


## -description




## -parameters




### -param dwCookie [in]

Contains a <i>DWORD</i> that identifies the advise sink to remove. This cookie is obtained when the advise sink is installed with <a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink</a> or <a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">ITfLangBarItemMgr::AdviseItemsSink</a>.


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




<a href="https://msdn.microsoft.com/a7fa257f-e600-4554-8b23-f73323f37e69">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/c01d80eb-9156-4fbf-98ff-7f06b145e72f">ITfLangBarItemMgr::AdviseItemSink
      </a>



<a href="https://msdn.microsoft.com/c0a3e86b-487b-410a-8bba-c2b5126126d2">
        ITfLangBarItemMgr::AdviseItemsSink
      </a>
 

 

