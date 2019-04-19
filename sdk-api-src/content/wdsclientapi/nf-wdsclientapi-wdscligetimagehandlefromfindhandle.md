---
UID: NF:wdsclientapi.WdsCliGetImageHandleFromFindHandle
title: WdsCliGetImageHandleFromFindHandle function (wdsclientapi.h)
author: windows-sdk-content
description: Returns an image handle for the current image in an image enumeration.
old-location: wds\wdscligetimagehandlefromfindhandle.htm
tech.root: wds
ms.assetid: 28cb93de-67f2-4e94-b0b7-0707c276662a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageHandleFromFindHandle, WdsCliGetImageHandleFromFindHandle function [Windows Deployment Services], wds.wdscligetimagehandlefromfindhandle, wdsclientapi/WdsCliGetImageHandleFromFindHandle
ms.topic: function
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsClientAPI.dll
api_name:
 - WdsCliGetImageHandleFromFindHandle
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliGetImageHandleFromFindHandle function


## -description


Returns an image handle for the current image in an image enumeration.  


## -parameters




### -param FindHandle [in]

A find handle returned by the <a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> function.


### -param phImageHandle [out]

A pointer to a location that contains an image handle for the current image referenced by the find handle.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



Use the <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function to close the image handle returned by this function.



