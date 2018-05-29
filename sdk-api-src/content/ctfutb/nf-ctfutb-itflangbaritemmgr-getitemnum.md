---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItemNum
title: ITfLangBarItemMgr::GetItemNum
author: windows-sdk-content
description: ITfLangBarItemMgr::GetItemNum method
old-location: tsf\itflangbaritemmgr_getitemnum.htm
old-project: TSF
ms.assetid: 0caf54b1-f862-4fc2-b593-c0e9f60d71cc
ms.author: windowssdkdev
ms.date: 05/23/2018
ms.keywords: GetItemNum, GetItemNum method [Text Services Framework], GetItemNum method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItemNum method, ITfLangBarItemMgr.GetItemNum, ITfLangBarItemMgr::GetItemNum, _tsf_itflangbaritemmgr_getitemnum_ref, ctfutb/ITfLangBarItemMgr::GetItemNum, tsf.itflangbaritemmgr_getitemnum
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
-	ITfLangBarItemMgr.GetItemNum
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItemMgr::GetItemNum


## -description




## -parameters




### -param pulCount [out]

Pointer to a <b>ULONG</b> that receives the number of items in the language bar.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pulCount</i> is invalid.

</td>
</tr>
</table>
 



