---
UID: NF:wdsclientapi.WdsCliGetImageHandleFromFindHandle
title: WdsCliGetImageHandleFromFindHandle function (wdsclientapi.h)
description: Returns an image handle for the current image in an image enumeration.
helpviewer_keywords: ["WdsCliGetImageHandleFromFindHandle","WdsCliGetImageHandleFromFindHandle function [Windows Deployment Services]","wds.wdscligetimagehandlefromfindhandle","wdsclientapi/WdsCliGetImageHandleFromFindHandle"]
old-location: wds\wdscligetimagehandlefromfindhandle.htm
tech.root: wds
ms.assetid: 28cb93de-67f2-4e94-b0b7-0707c276662a
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageHandleFromFindHandle, WdsCliGetImageHandleFromFindHandle function [Windows Deployment Services], wds.wdscligetimagehandlefromfindhandle, wdsclientapi/WdsCliGetImageHandleFromFindHandle
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
 - WdsCliGetImageHandleFromFindHandle
 - wdsclientapi/WdsCliGetImageHandleFromFindHandle
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
 - WdsCliGetImageHandleFromFindHandle
---

# WdsCliGetImageHandleFromFindHandle function


## -description

Returns an image handle for the current image in an image enumeration.

## -parameters

### -param FindHandle [in]

A find handle returned by the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.

### -param phImageHandle [out]

A pointer to a location that contains an image handle for the current image referenced by the find handle.

## -returns

If the function succeeds, the return is <b>S_OK</b>.

## -remarks

Use the <a href="/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function to close the image handle returned by this function.