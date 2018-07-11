---
UID: NF:cfapi.CfUpdateSyncProviderStatus
title: CfUpdateSyncProviderStatus function
author: windows-sdk-content
description: Updates the current status of the sync provider.
old-location: cloudapi\cfupdatesyncproviderstatus.htm
old-project: cfApi
ms.assetid: E0CB6CA2-439A-4919-95EF-B519ABBBB085
ms.author: windowssdkdev
ms.date: 02/27/2018
ms.keywords: CfUpdateSyncProviderStatus, CfUpdateSyncProviderStatus function, cfapi/CfUpdateSyncProviderStatus, cloudApi.cfupdatesyncproviderstatus
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.typenames: CF_UPDATE_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfUpdateSyncProviderStatus
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfUpdateSyncProviderStatus function


## -description


Updates the current status of the sync provider.


## -parameters




### -param ConnectionKey [in]

A connection key representing a communication channel with the sync filter.


### -param ProviderStatus [in]

The current status of the sync provider.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



