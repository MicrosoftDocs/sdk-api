---
UID: NF:wdstptmgmt.IWdsTransportClient.Disconnect
title: IWdsTransportClient::Disconnect
author: windows-sdk-content
description: Disconnects the WDS client from the session and specifies what action the client should take upon disconnection.
old-location: wds\iwdstransportclient_disconnect.htm
old-project: Wds
ms.assetid: faf3ab18-2629-402f-96ad-41337c165fba
ms.author: windowssdkdev
ms.date: 05/09/2018
ms.keywords: Disconnect, Disconnect method [Windows Deployment Services], Disconnect method [Windows Deployment Services],IWdsTransportClient interface, IWdsTransportClient interface [Windows Deployment Services],Disconnect method, IWdsTransportClient.Disconnect, IWdsTransportClient::Disconnect, wds.iwdstransportclient_disconnect, wdstptmgmt/IWdsTransportClient::Disconnect
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
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Wdstptmgmt.dll
api_name:
-	IWdsTransportClient.Disconnect
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportClient::Disconnect


## -description


Disconnects the WDS client from the session and specifies what action the client should take upon disconnection.


## -parameters




### -param DisconnectionType [in]

A value of the <a href="https://msdn.microsoft.com/f25bdc9e-0014-4ff7-bc01-8a13b6e3ace1">WDSTRANSPORT_DISCONNECT_TYPE</a> enumeration that specifies what action the WDS client should take when disconnected.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/39534411-3d69-408d-b495-10851fe40bdf">IWdsTransportClient</a>



<a href="https://msdn.microsoft.com/f25bdc9e-0014-4ff7-bc01-8a13b6e3ace1">WDSTRANSPORT_DISCONNECT_TYPE</a>
 

 

