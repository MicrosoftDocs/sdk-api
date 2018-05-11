---
UID: NN:wdstptmgmt.IWdsTransportServicePolicy2
title: IWdsTransportServicePolicy2
author: windows-driver-content
description: This interface inherits from the IWdsTransportServicePolicy interface and extends it beginning with Windows Server 2012.
old-location: wds\iwdstransportservicepolicy2.htm
old-project: Wds
ms.assetid: F03FC0C8-D589-4C3C-A6C1-AD631839ED26
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IWdsTransportServicePolicy2, IWdsTransportServicePolicy2 interface [Windows Deployment Services], IWdsTransportServicePolicy2 interface [Windows Deployment Services],described, wds.iwdstransportservicepolicy2, wdstptmgmt/IWdsTransportServicePolicy2
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportServicePolicy2
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportServicePolicy2 interface


## -description


This interface inherits from the <a href="https://msdn.microsoft.com/0a522633-87da-426c-9778-30949257e931">IWdsTransportServicePolicy</a> interface and extends it beginning with Windows Server 2012. 

A client application can obtain an interface pointer to an instance of the <b>IWdsTransportServicePolicy2</b> interface by first getting an interface pointer to the <a href="https://msdn.microsoft.com/0a522633-87da-426c-9778-30949257e931">IWdsTransportServicePolicy</a> interface  and then using the <a href="https://msdn.microsoft.com/54d5ff80-18db-43f2-b636-f93ac053146d">IUnknown::QueryInterface Method</a>. 


## -see-also




<a href="https://msdn.microsoft.com/0a522633-87da-426c-9778-30949257e931">IWdsTransportServicePolicy</a>



<a href="https://msdn.microsoft.com/3D8F193B-6EEA-4E40-A53C-EB0768E0DE83">WDSTRANSPORT_TFTP_CAPABILITY</a>
 

 

