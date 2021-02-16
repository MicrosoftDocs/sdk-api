---
UID: NF:wdstptmgmt.IWdsTransportManager.GetWdsTransportServer
title: IWdsTransportManager::GetWdsTransportServer (wdstptmgmt.h)
description: Creates an object of the IWdsTransportServer interface that can be used to manage a WDS transport server. The method confirms that the system can reach a WDS transport server with the specified name.
helpviewer_keywords: ["GetWdsTransportServer","GetWdsTransportServer method [Windows Deployment Services]","GetWdsTransportServer method [Windows Deployment Services]","IWdsTransportManager interface","IWdsTransportManager interface [Windows Deployment Services]","GetWdsTransportServer method","IWdsTransportManager.GetWdsTransportServer","IWdsTransportManager::GetWdsTransportServer","wds.iwdstransportmanager_getwdstransportserver","wdstptmgmt/IWdsTransportManager::GetWdsTransportServer"]
old-location: wds\iwdstransportmanager_getwdstransportserver.htm
tech.root: wds
ms.assetid: 537f75d1-43aa-4f18-a39b-ad45148c1246
ms.date: 12/05/2018
ms.keywords: GetWdsTransportServer, GetWdsTransportServer method [Windows Deployment Services], GetWdsTransportServer method [Windows Deployment Services],IWdsTransportManager interface, IWdsTransportManager interface [Windows Deployment Services],GetWdsTransportServer method, IWdsTransportManager.GetWdsTransportServer, IWdsTransportManager::GetWdsTransportServer, wds.iwdstransportmanager_getwdstransportserver, wdstptmgmt/IWdsTransportManager::GetWdsTransportServer
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
 - IWdsTransportManager::GetWdsTransportServer
 - wdstptmgmt/IWdsTransportManager::GetWdsTransportServer
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
 - IWdsTransportManager.GetWdsTransportServer
---

# IWdsTransportManager::GetWdsTransportServer


## -description

Creates an object of the <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a> interface that can be used to manage a WDS transport server. The method confirms that the system can reach a WDS transport server with the specified name.

## -parameters

### -param bszServerName [in]

The name of the WDS transport server to be represented by this object. This can be a NetBIOS name or a fully qualified DNS name. If the value is an empty string, the object represents the local computer.

### -param ppWdsTransportServer [out]

A pointer to the object of the  <a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a> interface.

## -returns

Standard HRESULT error values are used: S_OK for success; others for failure.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportmanager">IWdsTransportManager</a>



<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportserver">IWdsTransportServer</a>