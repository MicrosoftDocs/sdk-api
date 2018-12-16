---
UID: NF:wdspxe.PxeProviderUnRegister
title: PxeProviderUnRegister function
author: windows-sdk-content
description: Removes a provider from the list of registered providers.
old-location: wds\pxeproviderunregister.htm
tech.root: wds
ms.assetid: b468d865-c680-4f72-a10c-3d91542df8d3
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: PxeProviderUnRegister, PxeProviderUnRegister function [Windows Deployment Services], wds.pxeproviderunregister, wdspxe/PxeProviderUnRegister
ms.topic: function
req.header: wdspxe.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008, Windows Server 2003 with SP2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - WdsPxe.dll
api_name:
 - PxeProviderUnRegister
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PxeProviderUnRegister function


## -description


Removes a provider from the list of registered providers.


## -parameters




### -param pszProviderName [in]

Display name for provider from the call to the 
      <a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/2b377855-dae7-47cb-925a-9ee0a9265f83">PxeProviderRegister</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

