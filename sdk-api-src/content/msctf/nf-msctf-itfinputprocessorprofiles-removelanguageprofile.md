---
UID: NF:msctf.ITfInputProcessorProfiles.RemoveLanguageProfile
title: ITfInputProcessorProfiles::RemoveLanguageProfile
author: windows-sdk-content
description: ITfInputProcessorProfiles::RemoveLanguageProfile method
old-location: tsf\itfinputprocessorprofiles_removelanguageprofile.htm
tech.root: TSF
ms.assetid: 16eff9bc-1789-4bf6-b1ba-b7e8414ce080
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],RemoveLanguageProfile method, ITfInputProcessorProfiles.RemoveLanguageProfile, ITfInputProcessorProfiles::RemoveLanguageProfile, RemoveLanguageProfile, RemoveLanguageProfile method [Text Services Framework], RemoveLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_removelanguageprofile_ref, msctf/ITfInputProcessorProfiles::RemoveLanguageProfile, tsf.itfinputprocessorprofiles_removelanguageprofile
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - ITfInputProcessorProfiles.RemoveLanguageProfile
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfInputProcessorProfiles::RemoveLanguageProfile


## -description




## -parameters




### -param rclsid [in]

Contains the text service CLSID.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language identifier of the profile.


### -param guidProfile [out]

Contains a GUID value that identifies the language profile. This is the value specified in <a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile</a> when the profile was added.


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




<a href="https://msdn.microsoft.com/9fa722a4-1e3f-4845-aea7-3b24b517f2a5">ITfInputProcessorProfiles</a>



<a href="https://msdn.microsoft.com/d132bff1-24de-4e43-859b-2425ba7de8f0">ITfInputProcessorProfiles::AddLanguageProfile
      </a>
 

 

