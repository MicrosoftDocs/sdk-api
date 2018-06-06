---
UID: NF:wdsclientapi.WdsCliFreeStringArray
title: WdsCliFreeStringArray function
author: windows-sdk-content
description: This function can be used to free the array of string values that gets allocated by the WdsCliObtainDriverPackages function.
old-location: wds\wdsclifreestringarray.htm
old-project: Wds
ms.assetid: 37d96077-d3f0-4372-955d-f8c071d82230
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: WdsCliFreeStringArray, WdsCliFreeStringArray function [Windows Deployment Services], wds.wdsclifreestringarray, wdsclientapi/WdsCliFreeStringArray
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wdsclientapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - WdsCliFreeStringArray
product: Windows
targetos: Windows
req.lib: WdsClientAPI.lib
req.dll: WdsClientAPI.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# WdsCliFreeStringArray function


## -description


This function can be used to free the array of string values that gets allocated by the <a href="https://msdn.microsoft.com/2fb6bf5a-a46f-4664-be0a-6b4f2563986c">WdsCliObtainDriverPackages</a> function. 


## -parameters




### -param ppwszArray [in, out, optional]

Pointer to the array of string values being freed.


### -param ulCount [in]

Number of strings in the array that is pointed to by <i>ppwszArray</i>.


## -returns



If the function succeeds, the return is <b>S_OK</b>.



