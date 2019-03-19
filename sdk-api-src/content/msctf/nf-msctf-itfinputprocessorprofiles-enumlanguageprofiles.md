---
UID: NF:msctf.ITfInputProcessorProfiles.EnumLanguageProfiles
title: ITfInputProcessorProfiles::EnumLanguageProfiles (msctf.h)
author: windows-sdk-content
description: ITfInputProcessorProfiles::EnumLanguageProfiles method
old-location: tsf\itfinputprocessorprofiles_enumlanguageprofiles.htm
tech.root: TSF
ms.assetid: 9f7c970c-3f87-4f55-b13e-12fa8b89c362
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EnumLanguageProfiles, EnumLanguageProfiles method [Text Services Framework], EnumLanguageProfiles method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],EnumLanguageProfiles method, ITfInputProcessorProfiles.EnumLanguageProfiles, ITfInputProcessorProfiles::EnumLanguageProfiles, _tsf_itfinputprocessorprofiles_enumlanguageprofiles_ref, msctf/ITfInputProcessorProfiles::EnumLanguageProfiles, tsf.itfinputprocessorprofiles_enumlanguageprofiles
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
 - ITfInputProcessorProfiles.EnumLanguageProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfInputProcessorProfiles::EnumLanguageProfiles


## -description




## -parameters




### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language to obtain an enumerator for.


### -param ppEnum [out]

Pointer to an <a href="https://msdn.microsoft.com/8ac41bff-8537-4558-a92c-6e7dae6a6bdf">IEnumTfLanguageProfiles</a> interface pointer that receives the enumerator object.


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
No corresponding language profile was found in the operating system.<div> </div>-or-<div> </div> 
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




<a href="https://msdn.microsoft.com/8ac41bff-8537-4558-a92c-6e7dae6a6bdf">IEnumTfLanguageProfiles
      </a>



<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>
 

 

