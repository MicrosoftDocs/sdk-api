---
UID: NF:wdstptmgmt.IWdsTransportConfigurationManager.NotifyWdsTransportServices
title: IWdsTransportConfigurationManager::NotifyWdsTransportServices (wdstptmgmt.h)
author: windows-sdk-content
description: Sends a notification to WDS transport services. The notification value is translated to the appropriate WDS transport service controls, and then these controls are sent to the appropriate services.
old-location: wds\iwdstransportconfigurationmanager_notifywdstransportservices.htm
tech.root: wds
ms.assetid: 0ca38fe9-fc18-41f1-bd4b-5e3e84e496d0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWdsTransportConfigurationManager interface [Windows Deployment Services],NotifyWdsTransportServices method, IWdsTransportConfigurationManager.NotifyWdsTransportServices, IWdsTransportConfigurationManager::NotifyWdsTransportServices, NotifyWdsTransportServices, NotifyWdsTransportServices method [Windows Deployment Services], NotifyWdsTransportServices method [Windows Deployment Services],IWdsTransportConfigurationManager interface, wds.iwdstransportconfigurationmanager_notifywdstransportservices, wdstptmgmt/IWdsTransportConfigurationManager::NotifyWdsTransportServices
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
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportConfigurationManager.NotifyWdsTransportServices
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IWdsTransportConfigurationManager::NotifyWdsTransportServices


## -description


Sends a notification to WDS transport services. The notification value is translated to the appropriate WDS transport service controls, and then these controls are sent to the appropriate services.




## -parameters




### -param ServiceNotification [in]

A value of the <a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/ne-wdstptmgmt-__midl___midl_itf_wdstptmgmt_0000_0000_0005">WDSTRANSPORT_SERVICE_NOTIFICATION</a> enumeration that specifies the type of service notification to be sent.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportconfigurationmanager">IWdsTransportConfigurationManager</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wdstptmgmt/ne-wdstptmgmt-__midl___midl_itf_wdstptmgmt_0000_0000_0005">WDSTRANSPORT_SERVICE_NOTIFICATION</a>
 

 

