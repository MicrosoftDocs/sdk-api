---
UID: NF:cfapi.CfDisconnectSyncRoot
title: CfDisconnectSyncRoot function
author: windows-driver-content
description: Disconnects a communication channel created by CfConnectSyncRoot.
old-location: cloudapi\cfdisconnectsyncroot.htm
old-project: cfApi
ms.assetid: AB09804A-257B-49A2-861E-B6E102D45182
ms.author: windowsdriverdev
ms.date: 2/26/2018
ms.keywords: CfDisconnectSyncRoot, CfDisconnectSyncRoot function, cfapi/CfDisconnectSyncRoot, cloudApi.cfdisconnectsyncroot
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
-	CfDisconnectSyncRoot
product: Windows
targetos: Windows
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
---

# CfDisconnectSyncRoot function


## -description


Disconnects a communication channel created by <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a>.


## -parameters




### -param ConnectionKey [in]

The connection key returned from <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a> that is now used to disconnect the sync root.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This removes the communication channel with the platform that was previously established using <a href="https://msdn.microsoft.com/287DA978-9797-48DF-9C90-BA53BB82475C">CfConnectSyncRoot</a>. 

A sync provider can still receive callbacks during the <b>CfDisconnectSyncRoot</b> call, and the provider is free to choose whether the call needs to fail or be serviced. Either choice will not cause disruptions to the sync provider.

After a call to <b>CfDisconnectSyncRoot</b> returns, the sync provider will no longer receive callbacks and the platform will fail any operation that depends on said callbacks.

A sync provider should have WRITE_DATA or WRITE_DAC access to the sync root to be disconnected or a call to  <b>CfDisconnectSyncRoot</b> will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED). Also, if the sync root has not been previously connected, the call will be failed with invalid parameters.



