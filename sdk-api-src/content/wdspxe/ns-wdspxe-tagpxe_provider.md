---
UID: NS:wdspxe.tagPXE_PROVIDER
title: tagPXE_PROVIDER
author: windows-sdk-content
description: Describes a provider.
old-location: wds\pxe_provider.htm
old-project: wds
ms.assetid: a07afefd-7a97-42bb-8d70-2bc7c51ddef3
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PPXE_PROVIDER, PPXE_PROVIDER, PPXE_PROVIDER structure pointer [Windows Deployment Services], PXE_PROVIDER, PXE_PROVIDER structure [Windows Deployment Services], tagPXE_PROVIDER, wds.pxe_provider, wdspxe/PPXE_PROVIDER, wdspxe/PXE_PROVIDER"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
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
tech.root: 
req.typenames: PXE_PROVIDER, *PPXE_PROVIDER
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_PROVIDER
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagPXE_PROVIDER structure


## -description


Describes a provider.


## -struct-fields




### -field uSizeOfStruct

Size of the <b>PXE_PROVIDER</b> structure.


### -field pwszName

Address of a null-terminated string that specifies the display name of the provider. This name is displayed 
      to the user and must be unique among registered providers.


### -field pwszFilePath

Address of a null-terminated string that specifies the full path to the provider DLL.


### -field bIsCritical

Indicates whether the provider is critical. If a critical provider fails, the WDS server will also 
      fail.


### -field uIndex

Index of a provider in the list of registered providers.


## -see-also




<a href="https://msdn.microsoft.com/a76f2d7a-daf4-4258-9c6d-fd0d562f7efe">PxeProviderEnumNext</a>



<a href="https://msdn.microsoft.com/dd0f2b02-afc9-4ff6-b5b8-772ef15e4aa7">PxeProviderFreeInfo</a>



<a href="https://msdn.microsoft.com/2e52a6ae-cecb-45de-b777-108836ed5264">Windows Deployment Services Structures</a>
 

 

