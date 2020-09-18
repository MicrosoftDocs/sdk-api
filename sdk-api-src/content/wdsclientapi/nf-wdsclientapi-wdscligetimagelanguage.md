---
UID: NF:wdsclientapi.WdsCliGetImageLanguage
title: WdsCliGetImageLanguage function (wdsclientapi.h)
description: Returns the default language of the current image.
helpviewer_keywords: ["WdsCliGetImageLanguage","WdsCliGetImageLanguage function [Windows Deployment Services]","wds.wdscligetimagelanguage","wdsclientapi/WdsCliGetImageLanguage"]
old-location: wds\wdscligetimagelanguage.htm
tech.root: wds
ms.assetid: ac4d1f05-ab1c-4511-a3f1-205ab3280522
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageLanguage, WdsCliGetImageLanguage function [Windows Deployment Services], wds.wdscligetimagelanguage, wdsclientapi/WdsCliGetImageLanguage
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
 - WdsCliGetImageLanguage
 - wdsclientapi/WdsCliGetImageLanguage
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
 - WdsCliGetImageLanguage
---

# WdsCliGetImageLanguage function


## -description

Returns the default language of the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param ppwszValue [out]

A pointer to a pointer to a 
      null-terminated string value that contains the default language for the current image.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This value 
      is valid until the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function is used to change or close the 
      current handle.

## -see-also

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>