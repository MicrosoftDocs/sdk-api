---
UID: NF:msctf.ITfInputProcessorProfiles.EnableLanguageProfileByDefault
title: ITfInputProcessorProfiles::EnableLanguageProfileByDefault
author: windows-sdk-content
description: ITfInputProcessorProfiles::EnableLanguageProfileByDefault method
old-location: tsf\itfinputprocessorprofiles_enablelanguageprofilebydefault.htm
old-project: TSF
ms.assetid: 5ab40219-278d-4721-88a1-b0bd2e3d8d2f
ms.author: windowssdkdev
ms.date: 06/01/2018
ms.keywords: EnableLanguageProfileByDefault, EnableLanguageProfileByDefault method [Text Services Framework], EnableLanguageProfileByDefault method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],EnableLanguageProfileByDefault method, ITfInputProcessorProfiles.EnableLanguageProfileByDefault, ITfInputProcessorProfiles::EnableLanguageProfileByDefault, _tsf_itfinputprocessorprofiles_enablelanguageprofilebydefault_ref, msctf/ITfInputProcessorProfiles::EnableLanguageProfileByDefault, tsf.itfinputprocessorprofiles_enablelanguageprofilebydefault
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
 - ITfInputProcessorProfiles.EnableLanguageProfileByDefault
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfiles::EnableLanguageProfileByDefault


## -description




## -parameters




### -param rclsid [in]

Contains the CLSID of the text service of the profile to be enabled or disabled.


### -param langid [in]

Contains a <b>LANGID</b> value that specifies the language of the profile to be enabled or disabled.


### -param guidProfile [in]

Contains a GUID value that identifies the profile to be enabled or disabled.


### -param fEnable [in]

Contains a <b>BOOL</b> value that specifies if the profile is enabled or disabled. If this contains a nonzero value, the profile is enabled. If this contains zero, the profile is disabled.


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



<a href="https://msdn.microsoft.com/54aa6668-e577-4d75-9461-b604e1e73a78">ITfInputProcessorProfiles::EnableLanguageProfile
      </a>
 

 

