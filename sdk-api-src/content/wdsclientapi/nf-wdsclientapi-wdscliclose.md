---
UID: NF:wdsclientapi.WdsCliClose
title: WdsCliClose function (wdsclientapi.h)
author: windows-sdk-content
description: Closes a handle to a WDS session or image, and releases resources.
old-location: wds\wdscliclose.htm
tech.root: wds
ms.assetid: 6a833209-b7a0-40d8-8eca-43c08287d67e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliClose, WdsCliClose function [Windows Deployment Services], wds.wdscliclose, wdsclientapi/WdsCliClose
ms.topic: function
f1_keywords: 
 - "wdsclientapi/WdsCliClose"
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
 - WdsCliClose
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliClose function


## -description


Closes a handle to a WDS session or image, and releases resources.


## -parameters




### -param Handle [in]

 A handle to a WDS session or image. This function can close handles opened with the 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a> or 
      <a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a> functions.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclicreatesession">WdsCliCreateSession</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdsclientapi/nf-wdsclientapi-wdsclifindfirstimage">WdsCliFindFirstImage</a>



<a href="https://docs.microsoft.com/windows/desktop/Wds/windows-deployment-services-client-functions">Windows Deployment Services Client Functions</a>
 

 

