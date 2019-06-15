---
UID: NF:wdsclientapi.WdsCliFindNextImage
title: WdsCliFindNextImage function (wdsclientapi.h)
author: windows-sdk-content
description: Advances the reference of a find handle to the next image stored on a WDS server.
old-location: wds\wdsclifindnextimage.htm
tech.root: wds
ms.assetid: 15f2a00b-30bd-4736-b236-db847eec1779
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliFindNextImage, WdsCliFindNextImage function [Windows Deployment Services], wds.wdsclifindnextimage, wdsclientapi/WdsCliFindNextImage
ms.topic: function
f1_keywords: ["wdsclientapi/WdsCliFindNextImage"]
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
 - WdsCliFindNextImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliFindNextImage function


## -description


Advances the reference of a find handle to the next image stored on a WDS server.


## -parameters




### -param Handle [in]

The find handle returned by 
      the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function. If the <b>WdsCliFindNextImage</b> function is successful, the reference of the find handle is advanced to the next image stored on the WDS server.


## -returns



If the function succeeds, the return is <b>S_OK</b>.

If the function succeeds, and the end of the enumeration has been reached, the return is  <b>HRESULT_FROM_WIN32(ERROR_NO_MORE_FILES)</b>.




## -remarks



To enumerate all the images on a WDS Server, first get the WDS image find handle by calling the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> function, and then make repeated calls to <b>WdsCliFindNextImage</b> until the function returns <b>HRESULT_FROM_WIN32(ERROR_NO_MORE_FILES)</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>
 

 

