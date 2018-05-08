---
UID: NF:msctf.ITfInputProcessorProfiles.GetCurrentLanguage
title: ITfInputProcessorProfiles::GetCurrentLanguage
author: windows-driver-content
description: ITfInputProcessorProfiles::GetCurrentLanguage method
old-location: tsf\itfinputprocessorprofiles_getcurrentlanguage.htm
old-project: TSF
ms.assetid: c770872f-752f-4c34-8d0d-cdf3d5c7d6b4
ms.author: windowsdriverdev
ms.date: 3/26/2018
ms.keywords: GetCurrentLanguage, GetCurrentLanguage method [Text Services Framework], GetCurrentLanguage method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],GetCurrentLanguage method, ITfInputProcessorProfiles.GetCurrentLanguage, ITfInputProcessorProfiles::GetCurrentLanguage, _tsf_itfinputprocessorprofiles_getcurrentlanguage_ref, msctf/ITfInputProcessorProfiles::GetCurrentLanguage, tsf.itfinputprocessorprofiles_getcurrentlanguage
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
-	ITfInputProcessorProfiles.GetCurrentLanguage
product: Windows
targetos: Windows
req.lib: 
req.dll: Msctf.dll
req.irql: 
req.product: GDI+ 1.1
---

# ITfInputProcessorProfiles::GetCurrentLanguage


## -description




## -parameters




### -param plangid [out]

Pointer to a <b>LANGID</b> value that receives the language identifier of the currently active language.


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
<i>plangid</i> is invalid.

</td>
</tr>
</table>
 



