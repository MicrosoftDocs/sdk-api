---
UID: NF:wdsclientapi.WdsCliGetImagePath
title: WdsCliGetImagePath function (wdsclientapi.h)
description: Returns the path to the file that contains the current image.
helpviewer_keywords: ["WdsCliGetImagePath","WdsCliGetImagePath function [Windows Deployment Services]","wds.wdscligetimagepath","wdsclientapi/WdsCliGetImagePath"]
old-location: wds\wdscligetimagepath.htm
tech.root: wds
ms.assetid: 1ad28066-dcec-4dd4-896d-e009e6827ea3
ms.date: 12/05/2018
ms.keywords: WdsCliGetImagePath, WdsCliGetImagePath function [Windows Deployment Services], wds.wdscligetimagepath, wdsclientapi/WdsCliGetImagePath
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
 - WdsCliGetImagePath
 - wdsclientapi/WdsCliGetImagePath
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
 - WdsCliGetImagePath
---

# WdsCliGetImagePath function


## -description

Returns the path to the file that contains the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param ppwszValue [out]

A pointer to a pointer to a null-terminated string that contains the relative path of the image file for the current image.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

This value 
      is valid until the 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> or 
      <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function is used to change or close the 
      current handle.

To obtain the full path to the 
      image file, prefix the relative path returned in <i>ppWszValue</i> with "&#92;&#92;<i>Server</i>\\RemInst\".

## -see-also

<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a>



<a href="/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>