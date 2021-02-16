---
UID: NF:infotech.IStemmerConfig.SetLocaleInfo
title: IStemmerConfig::SetLocaleInfo (infotech.h)
description: Sets locale information for the stemmer.
helpviewer_keywords: ["IStemmerConfig interface [HTML Help Workshop]","SetLocaleInfo method","IStemmerConfig.SetLocaleInfo","IStemmerConfig::SetLocaleInfo","SetLocaleInfo","SetLocaleInfo method [HTML Help Workshop]","SetLocaleInfo method [HTML Help Workshop]","IStemmerConfig interface","htmlhelp.istemmerconfig_setlocaleinfo","infotech/IStemmerConfig::SetLocaleInfo","refIStemmerConfigSetLocaleInfo"]
old-location: htmlhelp\istemmerconfig_setlocaleinfo.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refistemmerconfigsetlocaleinfo.htm
ms.date: 12/05/2018
ms.keywords: IStemmerConfig interface [HTML Help Workshop],SetLocaleInfo method, IStemmerConfig.SetLocaleInfo, IStemmerConfig::SetLocaleInfo, SetLocaleInfo, SetLocaleInfo method [HTML Help Workshop], SetLocaleInfo method [HTML Help Workshop],IStemmerConfig interface, htmlhelp.istemmerconfig_setlocaleinfo, infotech/IStemmerConfig::SetLocaleInfo, refIStemmerConfigSetLocaleInfo
req.header: infotech.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStemmerConfig::SetLocaleInfo
 - infotech/IStemmerConfig::SetLocaleInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IStemmerConfig.SetLocaleInfo
---

# IStemmerConfig::SetLocaleInfo


## -description

Sets locale information for the stemmer.

## -parameters

### -param dwCodePageID [in]

ANSI code page number specified at build time.

### -param lcid [in]

Win32 API locale identifier specified at build time.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Locale described by the parameters is supported.



</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
Locale described by the parameters is not supported.



</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/api/infotech/nn-infotech-istemmerconfig">IStemmerConfig</a>