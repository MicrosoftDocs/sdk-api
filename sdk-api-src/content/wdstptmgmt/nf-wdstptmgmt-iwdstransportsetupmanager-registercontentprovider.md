---
UID: NF:wdstptmgmt.IWdsTransportSetupManager.RegisterContentProvider
title: IWdsTransportSetupManager::RegisterContentProvider
author: windows-sdk-content
description: Enables an application run on a client computer to register a content provider DLL. This makes the provider available for use by the WDS transport server.
old-location: wds\iwdstransportsetupmanager_registercontentprovider.htm
old-project: Wds
ms.assetid: c7793413-fef0-41e8-90f2-c8608f4ceb75
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IWdsTransportSetupManager interface [Windows Deployment Services],RegisterContentProvider method, IWdsTransportSetupManager.RegisterContentProvider, IWdsTransportSetupManager::RegisterContentProvider, RegisterContentProvider, RegisterContentProvider method [Windows Deployment Services], RegisterContentProvider method [Windows Deployment Services],IWdsTransportSetupManager interface, wds.iwdstransportsetupmanager_registercontentprovider, wdstptmgmt/IWdsTransportSetupManager::RegisterContentProvider
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportSetupManager.RegisterContentProvider
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
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


<b>HKLM</b>\<b>System</b>\<b>CurrentControlSet</b>\<b>Services</b>\<b>WDSServer</b>\<b>Providers</b>\<b>WDSMC</b>\<b>Providers</b>\<b><i>Content Provider Name (i.e. bszName)</i></b>\<b>AllowUnauth</b>






## -see-also




<a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a>
 

 

