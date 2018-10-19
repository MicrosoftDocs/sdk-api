---
UID: NF:ctffunc.ITfFnLangProfileUtil.RegisterActiveProfiles
title: ITfFnLangProfileUtil::RegisterActiveProfiles
author: windows-sdk-content
description: ITfFnLangProfileUtil::RegisterActiveProfiles method
old-location: tsf\itffnlangprofileutil_registeractiveprofiles.htm
tech.root: TSF
ms.assetid: 3b86206d-a299-4207-a0be-35a334786560
ms.author: windowssdkdev
ms.date: 10/18/2018
ms.keywords: ITfFnLangProfileUtil interface [Text Services Framework],RegisterActiveProfiles method, ITfFnLangProfileUtil.RegisterActiveProfiles, ITfFnLangProfileUtil::RegisterActiveProfiles, RegisterActiveProfiles, RegisterActiveProfiles method [Text Services Framework], RegisterActiveProfiles method [Text Services Framework],ITfFnLangProfileUtil interface, _tsf_itffnlangprofileutil_registeractiveprofiles_ref, ctffunc/ITfFnLangProfileUtil::RegisterActiveProfiles, tsf.itffnlangprofileutil_registeractiveprofiles
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Msctf.dll
api_name:
 - ITfFnLangProfileUtil.RegisterActiveProfiles
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnLangProfileUtil::RegisterActiveProfiles


## -description




## -parameters






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
 



