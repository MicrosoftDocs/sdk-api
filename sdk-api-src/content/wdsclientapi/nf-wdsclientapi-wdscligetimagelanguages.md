---
UID: NF:wdsclientapi.WdsCliGetImageLanguages
title: WdsCliGetImageLanguages function (wdsclientapi.h)
author: windows-sdk-content
description: Returns an array of languages supported by the current image.
old-location: wds\wdscligetimagelanguages.htm
tech.root: wds
ms.assetid: 2f027cf9-fad6-4ae6-98ac-83b9041c095e
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: WdsCliGetImageLanguages, WdsCliGetImageLanguages function [Windows Deployment Services], wds.wdscligetimagelanguages, wdsclientapi/WdsCliGetImageLanguages
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
 - WdsCliGetImageLanguages
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# WdsCliGetImageLanguages function


## -description


Returns an array of languages supported by the current image.


## -parameters




### -param hIfh [in]

A find handle returned by the <a href="https://msdn.microsoft.com/1c631022-4c2b-410d-ab24-d0b8f7df10a3">WdsCliFindFirstImage</a> function. The image referenced by the find handle can be advanced using the <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> function.


### -param pppszValues [out]

A pointer to a pointer to an array of null-terminated string values. Each element in the 
      array contains a language of the current 
      image. 


### -param pdwNumValues [out]

Pointer to a value that contains the number of languages in the <i>pppszValues</i> parameter. 


## -returns



If the function succeeds, the return is <b>S_OK</b>.




## -remarks



This value 
      is valid until the 
      <a href="https://msdn.microsoft.com/15f2a00b-30bd-4736-b236-db847eec1779">WdsCliFindNextImage</a> or 
      <a href="https://msdn.microsoft.com/6a833209-b7a0-40d8-8eca-43c08287d67e">WdsCliClose</a> function is used to change or close the 
      current handle.




## -see-also




<a href="https://msdn.microsoft.com/4cedd8a8-7f46-4229-9d96-58965b751e43">Windows Deployment Services Client Functions</a>
 

 

