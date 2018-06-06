---
UID: NN:wdstptmgmt.IWdsTransportSetupManager2
title: IWdsTransportSetupManager2
author: windows-sdk-content
description: This interface inherits from the IWdsTransportSetupManager interface and extends it. It is available beginning with Windows Server 2012.
old-location: wds\iwdstransportsetupmanager2.htm
old-project: Wds
ms.assetid: C16D037D-8E6C-4789-8947-D3BAC73D86FF
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: IWdsTransportSetupManager2, IWdsTransportSetupManager2 interface [Windows Deployment Services], IWdsTransportSetupManager2 interface [Windows Deployment Services],described, wds.iwdstransportsetupmanager2, wdstptmgmt/IWdsTransportSetupManager2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - IWdsTransportSetupManager2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportSetupManager2 interface


## -description


This interface inherits from the <a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a> interface and extends it. It is available beginning with Windows Server 2012. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportSetupManager2</b> interface by first getting an interface pointer to the <a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a> interface  and then using the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a>. 


## -see-also




<a href="https://msdn.microsoft.com/4a5c247f-28d7-4057-87e9-fca6e9effc96">IWdsTransportCollection</a>



<a href="https://msdn.microsoft.com/b7b0dc9f-081e-472f-98f7-fe555a411ea3">IWdsTransportSetupManager</a>
 

 

