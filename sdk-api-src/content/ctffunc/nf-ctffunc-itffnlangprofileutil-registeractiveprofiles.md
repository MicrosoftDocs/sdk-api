---
UID: NF:ctffunc.ITfFnLangProfileUtil.RegisterActiveProfiles
title: ITfFnLangProfileUtil::RegisterActiveProfiles (ctffunc.h)
description: ITfFnLangProfileUtil::RegisterActiveProfiles method
helpviewer_keywords: ["ITfFnLangProfileUtil interface [Text Services Framework]","RegisterActiveProfiles method","ITfFnLangProfileUtil.RegisterActiveProfiles","ITfFnLangProfileUtil::RegisterActiveProfiles","RegisterActiveProfiles","RegisterActiveProfiles method [Text Services Framework]","RegisterActiveProfiles method [Text Services Framework]","ITfFnLangProfileUtil interface","_tsf_itffnlangprofileutil_registeractiveprofiles_ref","ctffunc/ITfFnLangProfileUtil::RegisterActiveProfiles","tsf.itffnlangprofileutil_registeractiveprofiles"]
old-location: tsf\itffnlangprofileutil_registeractiveprofiles.htm
tech.root: TSF
ms.assetid: 3b86206d-a299-4207-a0be-35a334786560
ms.date: 12/05/2018
ms.keywords: ITfFnLangProfileUtil interface [Text Services Framework],RegisterActiveProfiles method, ITfFnLangProfileUtil.RegisterActiveProfiles, ITfFnLangProfileUtil::RegisterActiveProfiles, RegisterActiveProfiles, RegisterActiveProfiles method [Text Services Framework], RegisterActiveProfiles method [Text Services Framework],ITfFnLangProfileUtil interface, _tsf_itffnlangprofileutil_registeractiveprofiles_ref, ctffunc/ITfFnLangProfileUtil::RegisterActiveProfiles, tsf.itffnlangprofileutil_registeractiveprofiles
req.header: ctffunc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Ctffunc.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Msctf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
ms.custom: 19H1
f1_keywords:
 - ITfFnLangProfileUtil::RegisterActiveProfiles
 - ctffunc/ITfFnLangProfileUtil::RegisterActiveProfiles
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
 - ITfFnLangProfileUtil.RegisterActiveProfiles
---

# ITfFnLangProfileUtil::RegisterActiveProfiles


## -description

Causes the speech text service to register its active profiles.



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
<dt><b>S_FALSE</b></dt>
</dl>
</td>
<td width="60%">
The speech text service removed its active profiles based on user actions.

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

