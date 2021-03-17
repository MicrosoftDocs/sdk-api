---
UID: NF:wdstptmgmt.IWdsTransportSetupManager.RegisterContentProvider
title: IWdsTransportSetupManager::RegisterContentProvider (wdstptmgmt.h)
description: Enables an application run on a client computer to register a content provider DLL. This makes the provider available for use by the WDS transport server.
helpviewer_keywords: ["IWdsTransportSetupManager interface [Windows Deployment Services]","RegisterContentProvider method","IWdsTransportSetupManager.RegisterContentProvider","IWdsTransportSetupManager::RegisterContentProvider","RegisterContentProvider","RegisterContentProvider method [Windows Deployment Services]","RegisterContentProvider method [Windows Deployment Services]","IWdsTransportSetupManager interface","wds.iwdstransportsetupmanager_registercontentprovider","wdstptmgmt/IWdsTransportSetupManager::RegisterContentProvider"]
old-location: wds\iwdstransportsetupmanager_registercontentprovider.htm
tech.root: wds
ms.assetid: c7793413-fef0-41e8-90f2-c8608f4ceb75
ms.date: 12/05/2018
ms.keywords: IWdsTransportSetupManager interface [Windows Deployment Services],RegisterContentProvider method, IWdsTransportSetupManager.RegisterContentProvider, IWdsTransportSetupManager::RegisterContentProvider, RegisterContentProvider, RegisterContentProvider method [Windows Deployment Services], RegisterContentProvider method [Windows Deployment Services],IWdsTransportSetupManager interface, wds.iwdstransportsetupmanager_registercontentprovider, wdstptmgmt/IWdsTransportSetupManager::RegisterContentProvider
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportSetupManager::RegisterContentProvider
 - wdstptmgmt/IWdsTransportSetupManager::RegisterContentProvider
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportSetupManager.RegisterContentProvider
---

# IWdsTransportSetupManager::RegisterContentProvider


## -description

Enables an application run on a client computer to register a content provider DLL. This makes the provider available for use by the WDS transport server.

## -parameters

### -param bszName [in]

The name of the content provider to be registered. This name must be unique on the server.

### -param bszDescription [in]

A description of the content provider that can be  read by an administrator.

### -param bszFilePath [in]

The  full path to the DLL that implements the content provider. The path can include environment variables.

### -param bszInitializationRoutine [in]

The name of a function exported by the content provider that the WDS transport server can use to initialize the provider.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -remarks

To enable a multicast provider to support unauthenticated connections, the provider developer can add the <b>AllowUnAuth</b> key to the registry and set its <b>DWORD</b> value equal to 1.


<b>HKLM</b>&#92;<b>System</b>&#92;<b>CurrentControlSet</b>&#92;<b>Services</b>&#92;<b>WDSServer</b>&#92;<b>Providers</b>&#92;<b>WDSMC</b>&#92;<b>Providers</b>&#92;<b><i>Content Provider Name (i.e. bszName)</i></b>&#92;<b>AllowUnauth</b>

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportsetupmanager">IWdsTransportSetupManager</a>