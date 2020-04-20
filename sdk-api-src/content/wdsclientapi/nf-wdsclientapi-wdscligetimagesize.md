---
UID: NF:wdsclientapi.WdsCliGetImageSize
title: WdsCliGetImageSize function (wdsclientapi.h)
description: Returns the size of the current image.helpviewer_keywords: ["WdsCliGetImageSize","WdsCliGetImageSize function [Windows Deployment Services]","wds.wdscligetimagesize","wdsclientapi/WdsCliGetImageSize"]
old-location: wds\wdscligetimagesize.htm
tech.root: wds
ms.assetid: 35d04426-dfb4-48db-bb81-734d2d2ecdcb
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageSize, WdsCliGetImageSize function [Windows Deployment Services], wds.wdscligetimagesize, wdsclientapi/WdsCliGetImageSize
f1_keywords:
- wdsclientapi/WdsCliGetImageSize
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- DllExport
api_location:
- WdsClientAPI.dll
api_name:
- WdsCliGetImageSize
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliGetImageSize function


## -description


Returns the size of the current image.


## -parameters




### -param hIfh [in]

A find handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.


### -param pullValue [out]

A pointer to a value that contains the size of the current image. 


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
 

 

