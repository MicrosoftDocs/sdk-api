---
UID: NF:wdspxe.PxeProviderEnumClose
title: PxeProviderEnumClose function
author: windows-driver-content
description: Closes the enumeration of providers opened by the PxeProviderEnumFirst function.
old-location: wds\pxeproviderenumclose.htm
old-project: Wds
ms.assetid: 6b71c2cf-a156-4ccb-be7c-2955b4db26a2
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PxeProviderEnumClose, PxeProviderEnumClose function [Windows Deployment Services], wds.pxeproviderenumclose, wdspxe/PxeProviderEnumClose
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
req.typenames: WDS_CLI_CRED, *PWDS_CLI_CRED, *LPWDS_CLI_CRED
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	WdsPxe.dll
api_name:
-	PxeProviderEnumClose
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeProviderEnumClose function


## -description


Closes the enumeration of providers opened by the 
    <a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a> function.


## -parameters




### -param hEnum [in]

<b>HANDLE</b> returned by the 
      <a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

