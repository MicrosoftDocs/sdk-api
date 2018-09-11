---
UID: NF:ctfutb.ITfLangBarItemMgr.GetItems
title: ITfLangBarItemMgr::GetItems
author: windows-sdk-content
description: ITfLangBarItemMgr::GetItems method
old-location: tsf\itflangbaritemmgr_getitems.htm
tech.root: TSF
ms.assetid: b6342d4b-e2b6-47d7-9f66-b3aa329c480d
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetItems, GetItems method [Text Services Framework], GetItems method [Text Services Framework],ITfLangBarItemMgr interface, ITfLangBarItemMgr interface [Text Services Framework],GetItems method, ITfLangBarItemMgr.GetItems, ITfLangBarItemMgr::GetItems, _tsf_itflangbaritemmgr_getitems_ref, ctfutb/ITfLangBarItemMgr::GetItems, tsf.itflangbaritemmgr_getitems
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
 - ITfLangBarItemMgr.GetItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfLangBarItemMgr::GetItems


## -description




## -parameters




### -param ulCount [in]

Specifies the number of items to obtain the status for.


### -param ppItem [out]

Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a> interface pointers that receive the item interfaces. This array must be at least <i>ulCount</i> elements in length.


### -param pInfo

[in, out] Pointer to an array of <a href="https://msdn.microsoft.com/en-us/library/ms629074(v=VS.85).aspx">TF_LANGBARITEMINFO</a> structures that receive the information for each item. This array must be at least <i>ulCount</i> elements in length.


### -param pdwStatus

[in, out] Pointer to an array of <b>DWORD</b> values that receive the status of each item. Each element in this array receives zero or a combination of one or more of the <a href="https://msdn.microsoft.com/en-us/library/ms629077(v=VS.85).aspx">TF_LBI_STATUS_*</a> values. This array must be at least <i>ulCount</i> elements in length.


### -param pcFetched

[in, out] Pointer to a ULONG that receives the number of items obtained by this method. This parameter can be <b>NULL</b> if this information is not required.


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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of items obtained is less than the number of items requested. If <i>pcFetched</i> is not <b>NULL</b>, <i>pcFetched</i> receives the number of items obtained.

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




<a href="https://msdn.microsoft.com/en-us/library/ms628701(v=VS.85).aspx">ITfLangBarItem</a>



<a href="https://msdn.microsoft.com/en-us/library/ms628723(v=VS.85).aspx">ITfLangBarItemMgr</a>



<a href="https://msdn.microsoft.com/en-us/library/ms629074(v=VS.85).aspx">TF_LANGBARITEMINFO</a>



<a href="https://msdn.microsoft.com/5f2c0e61-f7e5-4dcc-86a3-7bd1c994b8bc">TF_LBI_STATUS_* Constants
      </a>
 

 

