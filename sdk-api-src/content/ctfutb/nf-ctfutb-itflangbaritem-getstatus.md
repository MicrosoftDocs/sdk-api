---
UID: NF:ctfutb.ITfLangBarItem.GetStatus
title: ITfLangBarItem::GetStatus
author: windows-sdk-content
description: ITfLangBarItem::GetStatus method
old-location: tsf\itflangbaritem_getstatus.htm
old-project: TSF
ms.assetid: 2f850553-ec79-4e2f-a4d5-c40dbaca0f01
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetStatus, GetStatus method [Text Services Framework], GetStatus method [Text Services Framework],ITfLangBarItem interface, ITfLangBarItem interface [Text Services Framework],GetStatus method, ITfLangBarItem.GetStatus, ITfLangBarItem::GetStatus, _tsf_itflangbaritem_getstatus_ref, ctfutb/ITfLangBarItem::GetStatus, tsf.itflangbaritem_getstatus
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
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfLangBarItem.GetStatus
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItem::GetStatus


## -description




## -parameters




### -param pdwStatus [out]

Pointer to a <b>DWORD</b> that receives zero or a combination of one or more of the <a href="https://msdn.microsoft.com/5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc">TF_LBI_STATUS_*</a> values that indicate the current status of the item.


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
<i>pdwStatus</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc">TF_LBI_STATUS_*
      </a>
 

 

