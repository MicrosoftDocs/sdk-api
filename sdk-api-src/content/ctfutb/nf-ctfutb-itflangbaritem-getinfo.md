---
UID: NF:ctfutb.ITfLangBarItem.GetInfo
title: ITfLangBarItem::GetInfo
author: windows-sdk-content
description: ITfLangBarItem::GetInfo method
old-location: tsf\itflangbaritem_getinfo.htm
old-project: TSF
ms.assetid: b32e433a-c0d6-418e-bf11-2291c85373c2
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: GetInfo, GetInfo method [Text Services Framework], GetInfo method [Text Services Framework],ITfLangBarItem interface, ITfLangBarItem interface [Text Services Framework],GetInfo method, ITfLangBarItem.GetInfo, ITfLangBarItem::GetInfo, _tsf_itflangbaritem_getinfo_ref, ctfutb/ITfLangBarItem::GetInfo, tsf.itflangbaritem_getinfo
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
 - Msctf.dll
api_name:
 - ITfLangBarItem.GetInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
---

# ITfLangBarItem::GetInfo


## -description




## -parameters




### -param pInfo [out]

Pointer to a <a href="https://msdn.microsoft.com/4a826a2c-4cae-4cbf-8a25-38337dcd498d">TF_LANGBARITEMINFO</a> structure that receives the language bar item information.


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
<i>pInfo</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/16612641-2bff-4e6f-a955-85793021a20b">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/4a826a2c-4cae-4cbf-8a25-38337dcd498d">TF_LANGBARITEMINFO
      </a>
 

 

