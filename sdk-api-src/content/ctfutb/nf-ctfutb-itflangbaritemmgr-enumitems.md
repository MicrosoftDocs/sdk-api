---
UID: NF:ctfutb.ITfLangBarItemMgr.EnumItems
title: ITfLangBarItemMgr::EnumItems
author: windows-sdk-content
description: ITfLangBarItemMgr::EnumItems method
old-location: tsf\itflangbaritemmgr_enumitems.htm
tech.root: TSF
ms.assetid: 90d61009-e0f7-4df6-a23b-1f9f489b15f9
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumItems, EnumItems method [Text Services Framework], EnumItems method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],EnumItems method, ITfLangBarItemMgr.EnumItems, ITfLangBarItemMgr::EnumItems, _tsf_itflangbaritemmgr_enumitems_ref, ctfutb/ITfLangBarItemMgr::EnumItems, tsf.itflangbaritemmgr_enumitems
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
 - ITfLangBarItemMgr.EnumItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemMgr::EnumItems


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/en-us/library/ms538185(v=VS.85).aspx">IEnumTfLangBarItems</a> interface pointer that receives the enumerator object.


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
<i>ppEnum</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
A memory allocation failure occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms538185(v=VS.85).aspx">IEnumTfLangBarItems</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628723(v=VS.85).aspx">ITfLangBarItemMgr</a>
 

 

