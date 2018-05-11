---
UID: NF:wdspxe.PxeProviderEnumNext
title: PxeProviderEnumNext function
author: windows-driver-content
description: Enumerates registered providers.
old-location: wds\pxeproviderenumnext.htm
old-project: Wds
ms.assetid: a76f2d7a-daf4-4258-9c6d-fd0d562f7efe
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: PxeProviderEnumNext, PxeProviderEnumNext function [Windows Deployment Services], wds.pxeproviderenumnext, wdspxe/PxeProviderEnumNext
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
-	PxeProviderEnumNext
product: Windows
targetos: Windows
req.lib: WdsPxe.lib
req.dll: WdsPxe.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# PxeProviderEnumNext function


## -description


Enumerates registered providers.


## -parameters




### -param hEnum [in]

<b>HANDLE</b> returned by the 
      <a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a> function.


### -param ppProvider [out]

Address of a <a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a> structure with the 
      <b>uSizeOfStruct</b> member filled in with the size of the structure. On return this 
      structure is filled in with provider information. This structure can be freed with the 
      <a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a> function.


## -returns



If the function succeeds, the return value is <b>ERROR_SUCCESS</b>.




## -see-also




<a href="https://msdn.microsoft.com/a07afefd-7a97-42bb-8d70-2bc7c51ddef3">PXE_PROVIDER</a>



<a href="https://msdn.microsoft.com/6b71c2cf-a156-4ccb-be7c-2955b4db26a2">PxeProviderEnumClose</a>



<a href="https://msdn.microsoft.com/b810455b-219b-49da-a4eb-c1a170711c68">PxeProviderEnumFirst</a>



<a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a>



<a href="https://msdn.microsoft.com/b6089ff9-4d74-4f5d-957f-4a741c09f4b9">Windows Deployment Services Server Functions</a>
 

 

