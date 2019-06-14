---
UID: NF:wdsclientapi.WdsCliFindFirstImage
title: WdsCliFindFirstImage function (wdsclientapi.h)
author: windows-sdk-content
description: Starts the enumeration of images stored on a WDS server and returns a find handle that references the first image.
old-location: wds\wdsclifindfirstimage.htm
tech.root: wds
ms.assetid: 1c631022-4c2b-410d-ab24-d0b8f7df10a3
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliFindFirstImage, WdsCliFindFirstImage function [Windows Deployment Services], wds.wdsclifindfirstimage, wdsclientapi/WdsCliFindFirstImage
ms.topic: function
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
 - WdsCliFindFirstImage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliFindFirstImage function


## -description


Starts the enumeration of images stored on a WDS server and returns a find handle that references the first image.


## -parameters




### -param hSession [in]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a> function.


### -param phFindHandle [out]

Pointer to a <b>HANDLE</b> value that receives the find handle. If the function succeeds, the find handle will reference the first image stored on the WDS server. If the function is unsuccessful, this parameter is unchanged. Use the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function to advance the reference of the find handle to the next image. 

<div class="alert"><b>Note</b>  Information about the image can only be obtained from the find handle by using the image information functions of the WDS client API.</div>
<div> </div>

## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



 The session must be authenticated to use this function. To authenticate an existing session, call the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdscliauthorizesession">WdsCliAuthorizeSession</a> function.

The WDS image find handle returned by this function can be used with the <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindnextimage">WdsCliFindNextImage</a> function to enumerate the images stored on the WDS server. 




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>
 

 

