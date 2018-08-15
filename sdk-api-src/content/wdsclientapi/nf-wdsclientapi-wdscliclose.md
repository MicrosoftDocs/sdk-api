---
UID: NF:wdsclientapi.WdsCliClose
title: WdsCliClose function
author: windows-sdk-content
description: Closes a handle to a WDS session or image, and releases resources.
old-location: wds\wdscliclose.htm
old-project: wds
ms.assetid: 6a833209-b7a0-40d8-8eca-43c08287d67e
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsCliClose, WdsCliClose function [Windows Deployment Services], wds.wdscliclose, wdsclientapi/WdsCliClose
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
 - WdsCliClose
product: Windows
targetos: Windows
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsCliClose function


## -description


Closes a handle to a WDS session or image, and releases resources.


## -parameters




### -param Handle [in]

 A handle to a WDS session or image. This function can close handles opened with the 
      <a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a> or 
      <a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a> functions.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -see-also




<a href="https://msdn.microsoft.com/c66801b2-ad5c-464b-ace3-269214621c20">WdsCliCreateSession</a>



<a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

