---
UID: NS:wdstpdi._WDS_TRANSPORTPROVIDER_INIT_PARAMS
title: "_WDS_TRANSPORTPROVIDER_INIT_PARAMS"
author: windows-sdk-content
description: This structure is used by the WdsTransportProviderInitialize callback function.
old-location: wds\wds_transportprovider_init_params.htm
old-project: Wds
ms.assetid: 5d89d192-7e60-4b5a-ba87-d5b30971a8a6
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: "*PWDS_TRANSPORTPROVIDER_INIT_PARAMS, PWDS_TRANSPORTPROVIDER_INIT_PARAMS, PWDS_TRANSPORTPROVIDER_INIT_PARAMS structure pointer [Windows Deployment Services], WDS_TRANSPORTPROVIDER_INIT_PARAMS, WDS_TRANSPORTPROVIDER_INIT_PARAMS structure [Windows Deployment Services], _WDS_TRANSPORTPROVIDER_INIT_PARAMS, wds.wds_transportprovider_init_params, wdstpdi/PWDS_TRANSPORTPROVIDER_INIT_PARAMS, wdstpdi/WDS_TRANSPORTPROVIDER_INIT_PARAMS"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wdstpdi.h
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
req.typenames: WDS_TRANSPORTPROVIDER_INIT_PARAMS, *PWDS_TRANSPORTPROVIDER_INIT_PARAMS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Wdstpdi.h
api_name:
-	WDS_TRANSPORTPROVIDER_INIT_PARAMS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _WDS_TRANSPORTPROVIDER_INIT_PARAMS structure


## -description


This structure is used by the <a href="https://msdn.microsoft.com/b7592e8d-6d7d-426a-8520-7b9cc5810d5a">WdsTransportProviderInitialize</a> callback function.


## -struct-fields




### -field ulLength

The length of this structure.


### -field ulMcServerVersion

The multicast server's version.


### -field hRegistryKey

An open handle to the registry key where this provider should
     store and retrieve its settings.


### -field hProvider

A handle that the provider can use to uniquely identify itself in calls to the multicast server.

