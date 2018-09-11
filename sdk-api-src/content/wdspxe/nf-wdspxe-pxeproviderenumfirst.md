---
UID: NF:wdspxe.PxeProviderEnumFirst
title: PxeProviderEnumFirst function
author: windows-sdk-content
description: Starts an enumeration of registered providers.
old-location: wds\pxeproviderenumfirst.htm
tech.root: Wds
ms.assetid: b810455b-219b-49da-a4eb-c1a170711c68
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: PxeProviderEnumFirst, PxeProviderEnumFirst function [Windows Deployment Services], wds.pxeproviderenumfirst, wdspxe/PxeProviderEnumFirst
ms.prod: windows-hardware
ms.technology: windows-devices
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
 - PxeProviderEnumFirst
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# PxeProviderEnumFirst function


## -description


Starts an enumeration of registered providers.


## -parameters




### -param phEnum [out]

Address of a <b>HANDLE</b> that on successful return can be used with the 
      <a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a> function to enumerate 
      providers. When the enumeration handle is no longer needed, use the 
      <a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a> function to close the 
      enumeration.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a>



<a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

