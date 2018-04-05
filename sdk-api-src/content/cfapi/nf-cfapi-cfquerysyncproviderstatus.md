---
UID: NF:cfapi.CfQuerySyncProviderStatus
title: CfQuerySyncProviderStatus function
author: windows-driver-content
description: Queries a sync provider to get the status of the provider.
old-location: cloudapi\cfquerysyncproviderstatus.htm
old-project: cfApi
ms.assetid: 02E6197B-D84A-4E3F-A74C-F5DACAA60AF9
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfQuerySyncProviderStatus, CfQuerySyncProviderStatus function, cfapi/CfQuerySyncProviderStatus, cloudApi.cfquerysyncproviderstatus
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: CF_PLACEHOLDER_RANGE_INFO_CLASS, *PCF_PLACEHOLDER_RANGE_INFO_CLASS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CldApi.dll
api_name:
-	CfQuerySyncProviderStatus
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfQuerySyncProviderStatus function


## -description


Queries a sync provider to get the status of the provider.


## -parameters




### -param ConnectionKey [in]

A connection key representing a communication channel with the sync filter.


### -param ProviderStatus [out]

The current status of the sync provider.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



