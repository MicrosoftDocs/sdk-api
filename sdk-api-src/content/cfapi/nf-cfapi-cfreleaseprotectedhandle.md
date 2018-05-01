---
UID: NF:cfapi.CfReleaseProtectedHandle
title: CfReleaseProtectedHandle function
author: windows-driver-content
description: Releases a protected handle referenced by CfReferenceProtectedHandle.
old-location: cloudapi\cfreleaseprotectedhandle.htm
old-project: cfApi
ms.assetid: BB63C5EE-92D7-4051-8198-09F50BBC75C5
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfReleaseProtectedHandle, CfReleaseProtectedHandle function, cfapi/CfReleaseProtectedHandle, cloudApi.cfreleaseprotectedhandle
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
req.typenames: CF_UPDATE_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	CldApi.dll
api_name:
-	CfReleaseProtectedHandle
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfReleaseProtectedHandle function


## -description


Releases a protected handle referenced by <a href="https://msdn.microsoft.com/C6281FD6-3A37-4D90-9B19-03DD23949C39">CfReferenceProtectedHandle</a>.


## -parameters




### -param ProtectedHandle [in]

The protected handle to be released.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



