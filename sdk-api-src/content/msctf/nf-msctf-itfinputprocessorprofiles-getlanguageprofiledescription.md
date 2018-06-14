---
UID: NF:msctf.ITfInputProcessorProfiles.GetLanguageProfileDescription
title: ITfInputProcessorProfiles::GetLanguageProfileDescription
author: windows-sdk-content
description: ITfInputProcessorProfiles::GetLanguageProfileDescription method
old-location: tsf\itfinputprocessorprofiles_getlanguageprofiledescription.htm
old-project: TSF
ms.assetid: f5838d26-1065-498c-8361-8929c07fc725
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: GetLanguageProfileDescription, GetLanguageProfileDescription method [Text Services Framework], GetLanguageProfileDescription method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetLanguageProfileDescription method, ITfInputProcessorProfiles.GetLanguageProfileDescription, ITfInputProcessorProfiles::GetLanguageProfileDescription, _tsf_itfinputprocessorprofiles_getlanguageprofiledescription_ref, msctf/ITfInputProcessorProfiles::GetLanguageProfileDescription, tsf.itfinputprocessorprofiles_getlanguageprofiledescription
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: TF_DA_ATTR_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputProcessorProfiles.GetLanguageProfileDescription
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfiles::GetLanguageProfileDescription


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service to obtain the profile description for.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies which language to obtain the profile description for.


### -param guidProfile [in]

Contains a GUID value that identifies the language to obtain the profile description for.


### -param pbstrProfile [out]

Pointer to a <b>BSTR</b> value that receives the description string. The caller is responsible for freeing this memory using <a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a> when it is no longer required.


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
<i>pbstrProfile</i> is invalid.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>



<a href="8f230ee3-5f6e-4cb9-a910-9c90b754dcd3">SysFreeString</a>
 

 

