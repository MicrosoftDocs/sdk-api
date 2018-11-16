---
UID: NF:msctf.ITfInputProcessorProfiles.ChangeCurrentLanguage
title: ITfInputProcessorProfiles::ChangeCurrentLanguage
author: windows-sdk-content
description: ITfInputProcessorProfiles::ChangeCurrentLanguage method
old-location: tsf\itfinputprocessorprofiles_changecurrentlanguage.htm
tech.root: TSF
ms.assetid: 2a0a6aa2-9015-4150-bbcf-e3f7218d53e8
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: ChangeCurrentLanguage, ChangeCurrentLanguage method [Text Services Framework], ChangeCurrentLanguage method [Text Services Framework],ITfInputProcessorProfiles interface, ITfInputProcessorProfiles interface [Text Services Framework],ChangeCurrentLanguage method, ITfInputProcessorProfiles.ChangeCurrentLanguage, ITfInputProcessorProfiles::ChangeCurrentLanguage, _tsf_itfinputprocessorprofiles_changecurrentlanguage_ref, msctf/ITfInputProcessorProfiles::ChangeCurrentLanguage, tsf.itfinputprocessorprofiles_changecurrentlanguage
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
 - ITfInputProcessorProfiles.ChangeCurrentLanguage
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
- apiref
: 
- COM
: 
- msctf.h
: 
- ITfInputProcessorProfiles.ChangeCurrentLanguage
: 
---

# ITfInputProcessorProfiles::ChangeCurrentLanguage


## -description




## -parameters




### -param langid [in]

Contains the <b>LANGID</b> of the language to make active.


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
<i>langid</i> is an invalid language identifier.

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
<tr>
<td width="40%">
<dl>
<dt><b>E_UNEXPECTED</b></dt>
</dl>
</td>
<td width="60%">
No thread manager was created for the calling thread.

</td>
</tr>
</table>
 



