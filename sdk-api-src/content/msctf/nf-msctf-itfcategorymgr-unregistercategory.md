---
UID: NF:msctf.ITfCategoryMgr.UnregisterCategory
title: ITfCategoryMgr::UnregisterCategory (msctf.h)
author: windows-sdk-content
description: ITfCategoryMgr::UnregisterCategory method
old-location: tsf\itfcategorymgr_unregistercategory.htm
tech.root: TSF
ms.assetid: 73013bc1-4623-4e00-b87b-29ea3d728e9f
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ITfCategoryMgr interface [Text Services Framework],UnregisterCategory method, ITfCategoryMgr.UnregisterCategory, ITfCategoryMgr::UnregisterCategory, UnregisterCategory, UnregisterCategory method [Text Services Framework], UnregisterCategory method [Text Services Framework],ITfCategoryMgr interface, _tsf_itfcategorymgr_unregistercategory_ref, msctf/ITfCategoryMgr::UnregisterCategory, tsf.itfcategorymgr_unregistercategory
ms.topic: method
f1_keywords: ["msctf/ITfCategoryMgr.UnregisterCategory"]
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
 - ITfCategoryMgr.UnregisterCategory
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
---

# ITfCategoryMgr::UnregisterCategory


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service that owns the item.


### -param rcatid [in]

Contains a GUID that identifies the category that the item is registered under.


### -param rguid [in]

Contains a GUID that identifies the item to remove.


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




<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nn-msctf-itfcategorymgr">ITfCategoryMgr
      </a>



<a href="https://docs.microsoft.com/windows/desktop/api/msctf/nf-msctf-itfcategorymgr-registercategory">ITfCategoryMgr::RegisterCategory
      </a>
 

 

