---
UID: NF:msctf.ITfInputProcessorProfileMgr.EnumProfiles
title: ITfInputProcessorProfileMgr::EnumProfiles (msctf.h)
description: The ITfInputProcessorProfileMgr::EnumProfiles method returns profiles to be enumerated.
helpviewer_keywords: ["EnumProfiles","EnumProfiles method [Text Services Framework]","EnumProfiles method [Text Services Framework]","ITfInputProcessorProfileMgr interface","ITfInputProcessorProfileMgr interface [Text Services Framework]","EnumProfiles method","ITfInputProcessorProfileMgr.EnumProfiles","ITfInputProcessorProfileMgr::EnumProfiles","msctf/ITfInputProcessorProfileMgr::EnumProfiles","tsf.itfinputprocessorprofilemgr_enumprofiles"]
old-location: tsf\itfinputprocessorprofilemgr_enumprofiles.htm
tech.root: TSF
ms.assetid: d4728d12-9073-41b8-94bc-eaf7c1df19b6
ms.date: 12/05/2018
ms.keywords: EnumProfiles, EnumProfiles method [Text Services Framework], EnumProfiles method [Text Services Framework],ITfInputProcessorProfileMgr interface, ITfInputProcessorProfileMgr interface [Text Services Framework],EnumProfiles method, ITfInputProcessorProfileMgr.EnumProfiles, ITfInputProcessorProfileMgr::EnumProfiles, msctf/ITfInputProcessorProfileMgr::EnumProfiles, tsf.itfinputprocessorprofilemgr_enumprofiles
req.header: msctf.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITfInputProcessorProfileMgr::EnumProfiles
 - msctf/ITfInputProcessorProfileMgr::EnumProfiles
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfInputProcessorProfileMgr.EnumProfiles
---

# ITfInputProcessorProfileMgr::EnumProfiles


## -description

The <b>ITfInputProcessorProfileMgr::EnumProfiles</b> method returns profiles to be enumerated.

## -parameters

### -param langid [in]

[in] langid of the profiles to be enumerated. If langid is 0, all profiles will be enumerated.

### -param ppEnum [out]

[out] The pointer to receive a pointer of <a href="/windows/desktop/api/msctf/nn-msctf-ienumtfinputprocessorprofiles">IEnumTfInputProcessorProfiles</a> interface.

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
One or more parameters are invalid.

</td>
</tr>
</table>