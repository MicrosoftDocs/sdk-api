---
UID: NF:wdsclientapi.WdsCliFindFirstImage
title: WdsCliFindFirstImage function
author: windows-sdk-content
description: Starts the enumeration of images stored on a WDS server and returns a find handle that references the first image.
old-location: wds\wdsclifindfirstimage.htm
old-project: wds
ms.assetid: 1c631022-4c2b-410d-ab24-d0b8f7df10a3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsCliFindFirstImage, WdsCliFindFirstImage function [Windows Deployment Services], wds.wdsclifindfirstimage, wdsclientapi/WdsCliFindFirstImage
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdsclientapi.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WAITCHAIN_NODE_INFO, *PWAITCHAIN_NODE_INFO
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
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsCliFindFirstImage function


## -description


Starts the enumeration of images stored on a WDS server and returns a find handle that references the first image.


## -parameters




### -param hSession [in]

A handle to a session   with a WDS server. This was a handle returned by 
      the <a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a> function.


### -param phFindHandle [out]

Pointer to a <b>HANDLE</b> value that receives the find handle. If the function succeeds, the find handle will reference the first image stored on the WDS server. If the function is unsuccessful, this parameter is unchanged. Use the <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> function to advance the reference of the find handle to the next image. 

<div class="alert"><b>Note</b>  Information about the image can only be obtained from the find handle by using the image information functions of the WDS client API.</div>
<div> </div>

## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



 The session must be authenticated to use this function. To authenticate an existing session, call the 
      <a href="https://msdn.microsoft.com/88e95fa8-1a83-4ef9-b486-c8086cb08116">WdsCliAuthorizeSession</a> function.

The WDS image find handle returned by this function can be used with the <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> function to enumerate the images stored on the WDS server. 




## -see-also




<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

