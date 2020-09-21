---
UID: NF:wdsclientapi.WdsCliGetImageIndex
title: WdsCliGetImageIndex function (wdsclientapi.h)
description: Returns the index within the Windows Imaging Format(WIM) file for the current image.
helpviewer_keywords: ["WdsCliGetImageIndex","WdsCliGetImageIndex function [Windows Deployment Services]","wds.wdscligetimageindex","wdsclientapi/WdsCliGetImageIndex"]
old-location: wds\wdscligetimageindex.htm
tech.root: wds
ms.assetid: e90750f0-5b45-40d5-ae6f-23b885cbe714
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageIndex, WdsCliGetImageIndex function [Windows Deployment Services], wds.wdscligetimageindex, wdsclientapi/WdsCliGetImageIndex
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
 - WdsCliGetImageIndex
 - wdsclientapi/WdsCliGetImageIndex
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
 - WdsCliGetImageIndex
---

# WdsCliGetImageIndex function


## -description

Returns the index within the Windows Imaging Format(WIM) file for the current image.

## -parameters

### -param hIfh [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param pdwValue [out]

A pointer to a 
      value that contains the image index for the current image WIM file.

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