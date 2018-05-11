---
UID: NF:msctf.ITfInputProcessorProfiles.IsEnabledLanguageProfile
title: ITfInputProcessorProfiles::IsEnabledLanguageProfile
author: windows-driver-content
description: ITfInputProcessorProfiles::IsEnabledLanguageProfile method
old-location: tsf\itfinputprocessorprofiles_isenabledlanguageprofile.htm
old-project: TSF
ms.assetid: 9daaa5bf-3eb8-416f-b7f5-9b10c04bceb0
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: ITfInputProcessorProfiles interface [Text Services Framework],IsEnabledLanguageProfile method, ITfInputProcessorProfiles.IsEnabledLanguageProfile, ITfInputProcessorProfiles::IsEnabledLanguageProfile, IsEnabledLanguageProfile, IsEnabledLanguageProfile method [Text Services Framework], IsEnabledLanguageProfile method [Text Services Framework],ITfInputProcessorProfiles interface, _tsf_itfinputprocessorprofiles_isenabledlanguageprofile_ref, msctf/ITfInputProcessorProfiles::IsEnabledLanguageProfile, tsf.itfinputprocessorprofiles_isenabledlanguageprofile
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
req.typenames: TF_DA_ATTR_INFO
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Msctf.dll
api_name:
-	ITfInputProcessorProfiles.IsEnabledLanguageProfile
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfiles::IsEnabledLanguageProfile


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service of the profile in question.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language of the profile in question.


### -param guidProfile [in]

Contains a GUID value that identifies the profile in question.


### -param pfEnable [out]

Pointer to a <b>BOOL</b> value that receives a value that specifies if the profile is enabled or disabled. If this receives a nonzero value, the profile is enabled. If this receives zero, the profile is disabled.


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
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfEnable</i> is invalid.

</td>
</tr>
</table>
 



