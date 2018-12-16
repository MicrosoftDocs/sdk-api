---
UID: NF:msctf.ITfInputProcessorProfiles.EnumInputProcessorInfo
title: ITfInputProcessorProfiles::EnumInputProcessorInfo
author: windows-sdk-content
description: ITfInputProcessorProfiles::EnumInputProcessorInfo method
old-location: tsf\itfinputprocessorprofiles_enuminputprocessorinfo.htm
tech.root: TSF
ms.assetid: 55b85ff3-35da-4126-861a-2aa4e2e8422f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumInputProcessorInfo, EnumInputProcessorInfo method [Text Services Framework], EnumInputProcessorInfo method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],EnumInputProcessorInfo method, ITfInputProcessorProfiles.EnumInputProcessorInfo, ITfInputProcessorProfiles::EnumInputProcessorInfo, _tsf_itfinputprocessorprofiles_enuminputprocessorinfo_ref, msctf/ITfInputProcessorProfiles::EnumInputProcessorInfo, tsf.itfinputprocessorprofiles_enuminputprocessorinfo
ms.topic: method
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - Msctf.dll
api_name:
 - ITfInputProcessorProfiles.EnumInputProcessorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfInputProcessorProfiles::EnumInputProcessorInfo


## -description




## -parameters




### -param ppEnum [out]

Pointer to an <b>IEnumGUID</b> interface pointer that receives the enumerator object. The enumerator contains the CLSID for each registered text service. The caller must release this object when it is no longer required.


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
A memory allocation error occurred.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>



<a href="https://msdn.microsoft.com/264bc32e-60a2-4dff-a212-5682d30a769e">ITfInputProcessorProfiles::Register
      </a>
 

 

