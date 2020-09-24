---
UID: NF:wdsclientapi.WdsCliGetImageLastModifiedTime
title: WdsCliGetImageLastModifiedTime function (wdsclientapi.h)
description: Returns the last-modification time of the current image.
helpviewer_keywords: ["WdsCliGetImageLastModifiedTime","WdsCliGetImageLastModifiedTime function [Windows Deployment Services]","wds.wdscligetimagelastmodifiedtime","wdsclientapi/WdsCliGetImageLastModifiedTime"]
old-location: wds\wdscligetimagelastmodifiedtime.htm
tech.root: wds
ms.assetid: b0554857-ffef-4f45-8aba-90512ce7f3b1
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageLastModifiedTime, WdsCliGetImageLastModifiedTime function [Windows Deployment Services], wds.wdscligetimagelastmodifiedtime, wdsclientapi/WdsCliGetImageLastModifiedTime
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
 - WdsCliGetImageLastModifiedTime
 - wdsclientapi/WdsCliGetImageLastModifiedTime
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
 - WdsCliGetImageLastModifiedTime
---

# WdsCliGetImageLastModifiedTime function


## -description

Returns the last-modification time of the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param ppSysTimeValue [out]

A pointer to a pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure that contains the last-modified time of the current image.

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