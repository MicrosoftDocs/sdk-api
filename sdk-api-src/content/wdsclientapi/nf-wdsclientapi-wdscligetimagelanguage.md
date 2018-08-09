---
UID: NF:wdsclientapi.WdsCliGetImageLanguage
title: WdsCliGetImageLanguage function
author: windows-sdk-content
description: Returns the default language of the current image.
old-location: wds\wdscligetimagelanguage.htm
old-project: wds
ms.assetid: ac4d1f05-ab1c-4511-a3f1-205ab3280522
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WdsCliGetImageLanguage, WdsCliGetImageLanguage function [Windows Deployment Services], wds.wdscligetimagelanguage, wdsclientapi/WdsCliGetImageLanguage
ms.prod: windows
ms.technology: windows-sdk
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
 - WdsCliGetImageLanguage
product: Windows
targetos: Windows
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsCliGetImageLanguage function


## -description


Returns the default language of the current image.


## -parameters




### -param hIfh [in]

A find handle returned by the <a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> function.


### -param ppwszValue [out]

A pointer to a pointer to a 
      null-terminated string value that contains the default language for the current image.


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This value 
      is valid until the 
      <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> or 
      <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function is used to change or close the 
      current handle.




## -see-also




<a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a>



<a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a>



<a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a>



<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

