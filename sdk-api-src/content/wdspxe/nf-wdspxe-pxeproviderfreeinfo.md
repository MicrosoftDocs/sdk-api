---
UID: NF:wdspxe.PxeProviderFreeInfo
title: PxeProviderFreeInfo function (wdspxe.h)
author: windows-sdk-content
description: Frees memory allocated by the PxeProviderEnumNext function.
old-location: wds\pxeproviderfreeinfo.htm
tech.root: wds
ms.assetid: dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: PxeProviderFreeInfo, PxeProviderFreeInfo function [Windows Deployment Services], wds.pxeproviderfreeinfo, wdspxe/PxeProviderFreeInfo
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
 - PxeProviderFreeInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# PxeProviderFreeInfo function


## -description


Frees memory allocated by the 
    <a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a> function.


## -parameters




### -param pProvider [in]

Address of a <a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a> structure returned from the 
      <a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a>



<a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

