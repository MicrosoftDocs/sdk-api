---
UID: NF:wdsclientapi.WdsCliGetImageVersion
title: WdsCliGetImageVersion function (wdsclientapi.h)
description: Returns the version of the current image.
helpviewer_keywords: ["WdsCliGetImageVersion","WdsCliGetImageVersion function [Windows Deployment Services]","wds.wdscligetimageversion","wdsclientapi/WdsCliGetImageVersion"]
old-location: wds\wdscligetimageversion.htm
tech.root: wds
ms.assetid: 50cd6ca0-dffd-452c-9e68-904037f71ccc
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageVersion, WdsCliGetImageVersion function [Windows Deployment Services], wds.wdscligetimageversion, wdsclientapi/WdsCliGetImageVersion
f1_keywords:
- wdsclientapi/WdsCliGetImageVersion
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
- WdsCliGetImageVersion
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliGetImageVersion function


## -description


Returns the version of the current image.


## -parameters




### -param hIfh [in]

A find handle returned by the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function.


### -param ppwszValue [out]

A pointer to a pointer to a null-terminated string value that contains the version of the current version.


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
 

 

