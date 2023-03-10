---
UID: NF:wdstptmgmt.IWdsTransportConfigurationManager.RestartWdsTransportServices
title: IWdsTransportConfigurationManager::RestartWdsTransportServices (wdstptmgmt.h)
description: Stops and then restarts any WDS transport services that are running. If no services are running, the method returns with S_OK without further action.
helpviewer_keywords: ["IWdsTransportConfigurationManager interface [Windows Deployment Services]","RestartWdsTransportServices method","IWdsTransportConfigurationManager.RestartWdsTransportServices","IWdsTransportConfigurationManager::RestartWdsTransportServices","RestartWdsTransportServices","RestartWdsTransportServices method [Windows Deployment Services]","RestartWdsTransportServices method [Windows Deployment Services]","IWdsTransportConfigurationManager interface","wds.iwdstransportconfigurationmanager_restartwdstransportservices","wdstptmgmt/IWdsTransportConfigurationManager::RestartWdsTransportServices"]
old-location: wds\iwdstransportconfigurationmanager_restartwdstransportservices.htm
tech.root: wds
ms.assetid: f0aa84fa-f2a6-4494-8994-89854565fd7b
ms.date: 12/05/2018
ms.keywords: IWdsTransportConfigurationManager interface [Windows Deployment Services],RestartWdsTransportServices method, IWdsTransportConfigurationManager.RestartWdsTransportServices, IWdsTransportConfigurationManager::RestartWdsTransportServices, RestartWdsTransportServices, RestartWdsTransportServices method [Windows Deployment Services], RestartWdsTransportServices method [Windows Deployment Services],IWdsTransportConfigurationManager interface, wds.iwdstransportconfigurationmanager_restartwdstransportservices, wdstptmgmt/IWdsTransportConfigurationManager::RestartWdsTransportServices
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
 - IWdsTransportConfigurationManager::RestartWdsTransportServices
 - wdstptmgmt/IWdsTransportConfigurationManager::RestartWdsTransportServices
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
 - IWdsTransportConfigurationManager.RestartWdsTransportServices
---

# IWdsTransportConfigurationManager::RestartWdsTransportServices


## -description

Stops and then restarts any WDS transport services that are running. If no services are running, the method returns with <b>S_OK</b>  without further action.



## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a>
