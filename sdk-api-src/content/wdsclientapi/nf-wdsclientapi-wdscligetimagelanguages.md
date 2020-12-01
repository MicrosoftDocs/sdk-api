---
UID: NF:wdsclientapi.WdsCliGetImageLanguages
title: WdsCliGetImageLanguages function (wdsclientapi.h)
description: Returns an array of languages supported by the current image.
helpviewer_keywords: ["WdsCliGetImageLanguages","WdsCliGetImageLanguages function [Windows Deployment Services]","wds.wdscligetimagelanguages","wdsclientapi/WdsCliGetImageLanguages"]
old-location: wds\wdscligetimagelanguages.htm
tech.root: wds
ms.assetid: 2f027cf9-fad6-4ae6-98ac-83b9041c095e
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageLanguages, WdsCliGetImageLanguages function [Windows Deployment Services], wds.wdscligetimagelanguages, wdsclientapi/WdsCliGetImageLanguages
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - WdsCliGetImageLanguages
 - wdsclientapi/WdsCliGetImageLanguages
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliGetImageLanguages
---

# WdsCliGetImageLanguages function


## -description

Returns an array of languages supported by the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param pppszValues [out]

A pointer to a pointer to an array of null-terminated string values. Each element in the 
      array contains a language of the current 
      image.

### -param pdwNumValues [out]

Pointer to a value that contains the number of languages in the <i>pppszValues</i> parameter.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This value 
      is valid until the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function is used to change or close the 
      current handle.

## -see-also

<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>