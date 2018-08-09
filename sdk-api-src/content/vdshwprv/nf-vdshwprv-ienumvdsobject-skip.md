---
UID: NF:vdshwprv.IEnumVdsObject.Skip
title: IEnumVdsObject::Skip
author: windows-sdk-content
description: Skips a specified number of objects in the enumeration.
old-location: base\ienumvdsobject_skip.htm
old-project: vds
ms.assetid: 8c0a856e-831e-489d-9e2a-bf2829bf59b6
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IEnumVdsObject interface [VDS],Skip method, IEnumVdsObject.Skip, IEnumVdsObject::Skip, Skip, Skip method [VDS], Skip method [VDS],IEnumVdsObject interface, base.ienumvdsobject_skip, vds/IEnumVdsObject::Skip, vdshwprv/IEnumVdsObject::Skip
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: vdshwprv.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: VDS_VERSION_SUPPORT_FLAG
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uuid.lib
 - Uuid.dll
api_name:
 - IEnumVdsObject.Skip
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: 
req.irql: 
req.product: Windows UI
---

# IEnumVdsObject::Skip


## -description


<p class="CCE_Message">[Beginning with Windows 8 and Windows Server 2012, the <a href="https://msdn.microsoft.com/536aafd2-cc04-48cc-8ee7-920efbba2a5f">Virtual Disk Service</a> COM interface is superseded by the <a href="https://msdn.microsoft.com/ff5e492d-5e62-4c9b-8f55-07859c9fee83">Windows Storage Management API</a>.]

Skips a specified number of 
   objects in the enumeration.


## -parameters




### -param celt [in]

The number of objects to skip.


## -returns



This method can return standard HRESULT values, such as E_INVALIDARG or E_OUTOFMEMORY, and <a href="https://msdn.microsoft.com/c9ddd3b7-f017-4880-976a-c879a40dc17b">VDS-specific return values</a>. It can also return converted <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">system error codes</a>  using the <a href="_com_hresult_from_win32">HRESULT_FROM_WIN32</a> macro. Errors can originate from VDS itself or from the underlying <a href="https://msdn.microsoft.com/b2f7628c-b567-40a9-9ad7-6c47077af5fb">VDS provider</a> that is being used. Possible return values include the following.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method skipped the specified number of objects. The number of skipped objects equals 
        <i>celt</i>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The number of objects specified is greater than the number of objects remaining. If the number of objects 
        remaining is less than the number specified in <i>celt</i>, the 
        <a href="https://msdn.microsoft.com/library/windows/hardware/dn926952">Skip</a> method skips all remaining 
        objects.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/08379071-b3cc-495a-bc8e-ad6cfacd432c">IEnumVdsObject</a>
 

 

