---
UID: NF:ctffunc.ITfFnLangProfileUtil.IsProfileAvailableForLang
title: ITfFnLangProfileUtil::IsProfileAvailableForLang
author: windows-sdk-content
description: ITfFnLangProfileUtil::IsProfileAvailableForLang method
old-location: tsf\itffnlangprofileutil_isprofileavailableforlang.htm
tech.root: TSF
ms.assetid: a0525a1b-e23c-49af-954d-e2d190c2f520
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: ITfFnLangProfileUtil interface [Text Services Framework],IsProfileAvailableForLang method, ITfFnLangProfileUtil.IsProfileAvailableForLang, ITfFnLangProfileUtil::IsProfileAvailableForLang, IsProfileAvailableForLang, IsProfileAvailableForLang method [Text Services Framework], IsProfileAvailableForLang method [Text Services Framework],ITfFnLangProfileUtil interface, _tsf_itffnlangprofileutil_isprofileavailableforlang_ref, ctffunc/ITfFnLangProfileUtil::IsProfileAvailableForLang, tsf.itffnlangprofileutil_isprofileavailableforlang
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
 - ITfFnLangProfileUtil.IsProfileAvailableForLang
product: Windows
targetos: Windows
req.typenames: 
req.redist: TSF 1.0 on Windows 2000 Professional
---

# ITfFnLangProfileUtil::IsProfileAvailableForLang


## -description




## -parameters




### -param langid [in]

Contains a <b>LANGID</b> that specifies the language that the query applies to.


### -param pfAvailable [out]

Pointer to a <b>BOOL</b> that receives nonzero if a profile is available for the language identified by langid or zero otherwise.


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
<i>pfAvailable</i> is invalid.

</td>
</tr>
</table>
 



