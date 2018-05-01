---
UID: NF:infotech.IStemmerConfig.SetLocaleInfo
title: IStemmerConfig::SetLocaleInfo method
author: windows-driver-content
description: Sets locale information for the stemmer.
old-location: htmlhelp\istemmerconfig_setlocaleinfo.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refistemmerconfigsetlocaleinfo.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IStemmerConfig, IStemmerConfig interface [HTML Help Workshop], SetLocaleInfo method, IStemmerConfig::SetLocaleInfo, SetLocaleInfo method [HTML Help Workshop], SetLocaleInfo method [HTML Help Workshop], IStemmerConfig interface, SetLocaleInfo,IStemmerConfig.SetLocaleInfo, htmlhelp.istemmerconfig_setlocaleinfo, infotech/IStemmerConfig::SetLocaleInfo, refIStemmerConfigSetLocaleInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IStemmerConfig.SetLocaleInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IStemmerConfig::SetLocaleInfo method


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




<a href="https://msdn.microsoft.com/3cdb1f6c-157e-4b6c-8536-9af43e79b08a">IStemmerConfig</a>
 

 

