---
UID: NF:msctf.ITfCategoryMgr.GetGUID
title: ITfCategoryMgr::GetGUID
author: windows-sdk-content
description: ITfCategoryMgr::GetGUID method
old-location: tsf\itfcategorymgr_getguid.htm
tech.root: TSF
ms.assetid: a5f5a67c-3152-4933-8a35-0a0cd555a0bf
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetGUID, GetGUID method [Text Services Framework], GetGUID method [Text Services Framework],ITfCategoryMgr interface, ITfCategoryMgr interface [Text Services Framework],GetGUID method, ITfCategoryMgr.GetGUID, ITfCategoryMgr::GetGUID, _tsf_itfcategorymgr_getguid_ref, msctf/ITfCategoryMgr::GetGUID, tsf.itfcategorymgr_getguid
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfCategoryMgr.GetGUID
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfCategoryMgr::GetGUID


## -description




## -parameters




### -param guidatom [in]

Contains a <b>TfGuidAtom</b> value that specifies the GUID to obtain.


### -param pguid [out]

Pointer to a <b>GUID</b> value that receives the <b>GUID</b> for the specified atom. Receives GUID_NULL if the <b>GUID</b> for the atom cannot be found.


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
<i>pguid</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/26139c8c-e1d9-4d7a-a0c0-ef73e572fbe4">ITfCategoryMgr
      </a>



<a href="https://msdn.microsoft.com/d0de17d9-be3a-4f68-a77d-880047775952">ITfCategoryMgr::RegisterGUID
      </a>



<a href="https://msdn.microsoft.com/91696612-1829-4052-81d1-eddc23278d35">TfGuidAtom
      </a>
 

 

