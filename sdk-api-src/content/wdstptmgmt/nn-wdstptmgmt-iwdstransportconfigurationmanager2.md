---
UID: NN:wdstptmgmt.IWdsTransportConfigurationManager2
title: IWdsTransportConfigurationManager2
author: windows-driver-content
description: This interface inherits from the IWdsTransportConfigurationManager interface and extends it with configuration settings, such as multicast session policy, that are available beginning with Windows Server 2008 R2.
old-location: wds\iwdstransportconfigurationmanager2.htm
old-project: Wds
ms.assetid: 93e22735-83a4-4037-abea-b72277f8b857
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IWdsTransportConfigurationManager2, IWdsTransportConfigurationManager2 interface [Windows Deployment Services], IWdsTransportConfigurationManager2 interface [Windows Deployment Services],described, wds.iwdstransportconfigurationmanager2, wdstptmgmt/IWdsTransportConfigurationManager2
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportConfigurationManager2
-	IWdsTransportConfigurationManager2.MulticastSessionPolicy
-	IWdsTransportConfigurationManager2.get_MulticastSessionPolicy
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportConfigurationManager2 interface


## -description


This interface inherits from the <a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a> interface and extends it with configuration settings, such as multicast session policy, that are available beginning with Windows Server 2008 R2. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportConfigurationManager2</b> interface by first getting an interface pointer to the <a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a> interface  and then using the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a>. 


## -see-also




<a href="https://msdn.microsoft.com/b86f9bc7-ddee-4d18-b5cb-28d28fa7ae7e">IWdsTransportConfigurationManager</a>
 

 

