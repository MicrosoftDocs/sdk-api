---
UID: NF:msctf.ITfCategoryMgr.RegisterGUID
title: ITfCategoryMgr::RegisterGUID
author: windows-sdk-content
description: ITfCategoryMgr::RegisterGUID method
old-location: tsf\itfcategorymgr_registerguid.htm
old-project: TSF
ms.assetid: d0de17d9-be3a-4f68-a77d-880047775952
ms.author: windowssdkdev
ms.date: 06/28/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],RegisterGUID method, ITfCategoryMgr.RegisterGUID, ITfCategoryMgr::RegisterGUID, RegisterGUID, RegisterGUID method [Text Services Framework], RegisterGUID method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_registerguid_ref, msctf/ITfCategoryMgr::RegisterGUID, tsf.itfcategorymgr_registerguid
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Msctf.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msctf.dll
api_name:
 - ITfCategoryMgr.RegisterGUID
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfCategoryMgr::RegisterGUID


## -description




## -parameters




### -param rguid [in]

Contains the GUID to obtain the identifier for.


### -param pguidatom [out]

Pointer to a <a href="https://msdn.microsoft.com/91696612-1829-4052-81d1-eddc23278d35">TfGuidAtom</a> value that receives the identifier of the GUID.


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
<i>pguidatom</i> is invalid.

</td>
</tr>
</table>
 




## -remarks



Identical <b>GUID</b> values receive identical <b>TfGuidAtom</b> values.

A <b>TfGuidAtom</b> value is only valid within the process that <b>ITfCategoryMgr::RegisterGUID</b> is called from.




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">
        ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/a5f5a67c-3152-4933-8a35-0a0cd555a0bf">
        ITfCategoryMgr::GetGUID
      </a>



<a href="https://msdn.microsoft.com/813916f6-610f-4031-bb17-67d7f5ffed6f">
        ITfCategoryMgr::IsEqualTfGuidAtom
      </a>



<a href="https://msdn.microsoft.com/91696612-1829-4052-81d1-eddc23278d35">TfGuidAtom
      </a>
 

 

