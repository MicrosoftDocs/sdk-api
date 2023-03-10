---
UID: NF:cfapi.CfDisconnectSyncRoot
title: CfDisconnectSyncRoot function (cfapi.h)
description: Disconnects a communication channel created by CfConnectSyncRoot.
helpviewer_keywords: ["CfDisconnectSyncRoot","CfDisconnectSyncRoot function","cfapi/CfDisconnectSyncRoot","cloudApi.cfdisconnectsyncroot"]
old-location: cloudapi\cfdisconnectsyncroot.htm
tech.root: cloudapi
ms.assetid: AB09804A-257B-49A2-861E-B6E102D45182
ms.date: 12/05/2018
ms.keywords: CfDisconnectSyncRoot, CfDisconnectSyncRoot function, cfapi/CfDisconnectSyncRoot, cloudApi.cfdisconnectsyncroot
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
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - CfDisconnectSyncRoot
 - cfapi/CfDisconnectSyncRoot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfDisconnectSyncRoot
---

# CfDisconnectSyncRoot function


## -description

Disconnects a communication channel created by <a href="/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot">CfConnectSyncRoot</a>.

## -parameters

### -param ConnectionKey [in]

The connection key returned from <a href="/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot">CfConnectSyncRoot</a> that is now used to disconnect the sync root.

## -returns

If this function succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This removes the communication channel with the platform that was previously established using <a href="/windows/desktop/api/cfapi/nf-cfapi-cfconnectsyncroot">CfConnectSyncRoot</a>. 

A sync provider can still receive callbacks during the <b>CfDisconnectSyncRoot</b> call, and the provider is free to choose whether the call needs to fail or be serviced. Either choice will not cause disruptions to the sync provider.

After a call to <b>CfDisconnectSyncRoot</b> returns, the sync provider will no longer receive callbacks and the platform will fail any operation that depends on said callbacks.

A sync provider should have WRITE_DATA or WRITE_DAC access to the sync root to be disconnected or a call to  <b>CfDisconnectSyncRoot</b> will be failed with HRESULT(ERROR_CLOUD_FILE_ACCESS_DENIED). Also, if the sync root has not been previously connected, the call will be failed with invalid parameters.