---
UID: NF:wdsclientapi.WdsCliGetImageNamespace
title: WdsCliGetImageNamespace function (wdsclientapi.h)
author: windows-sdk-content
description: Returns the namespace of the current image.
old-location: wds\wdscligetimagenamespace.htm
tech.root: wds
ms.assetid: 30396f0b-77bb-4c43-86a0-2d4454a05b72
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageNamespace, WdsCliGetImageNamespace function [Windows Deployment Services], wds.wdscligetimagenamespace, wdsclientapi/WdsCliGetImageNamespace
ms.topic: function
f1_keywords: 
 - "wdsclientapi/WdsCliGetImageNamespace"
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
req.lib: WdsClientApi.lib
req.dll: WdsClientApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientApi.dll
api_name:
 - WdsCliGetImageNamespace
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliGetImageNamespace function


## -description


Returns the namespace of the current image.


## -parameters




### -param hIfh [in]

A find handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.


### -param ppwszValue [out]

A pointer to a pointer to a 
      null-terminated string value that contains the namespace of the current image. If there is no namespace associated with this image, this returns null or an empty string.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This value 
      is valid until the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> or 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a> function is used to change or close the 
      current handle.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliclose">WdsCliClose</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>
 

 

