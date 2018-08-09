---
UID: NF:wdstptmgmt.IWdsTransportContent.RetrieveSessions
title: IWdsTransportContent::RetrieveSessions
author: windows-sdk-content
description: Retrieves a collection of active transport sessions associated with this content.
old-location: wds\iwdstransportcontent_retrievesessions.htm
old-project: wds
ms.assetid: 8901f9c5-931e-40d5-8a5c-d3a814556400
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWdsTransportContent interface [Windows Deployment Services],RetrieveSessions method, IWdsTransportContent.RetrieveSessions, IWdsTransportContent::RetrieveSessions, RetrieveSessions, RetrieveSessions method [Windows Deployment Services], RetrieveSessions method [Windows Deployment Services],IWdsTransportContent interface, wds.iwdstransportcontent_retrievesessions, wdstptmgmt/IWdsTransportContent::RetrieveSessions
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
 - IWdsTransportContent.RetrieveSessions
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportContent::RetrieveSessions


## -description


Retrieves a collection of active transport sessions associated with this content.


## -parameters




### -param ppWdsTransportSessions [out]

A pointer to a collection of objects of the <a href="https://msdn.microsoft.com/acf417ea-2396-4178-84e5-6d6b495476f8">IWdsTransportSession</a> interface that represent active sessions under this content.


## -returns



Standard HRESULT error values are used: S_OK for success; others for failure.




## -see-also




<a href="https://msdn.microsoft.com/d7ed1f64-578f-4b3a-b9af-9a48800b9ca4">IWdsTransportContent</a>
 

 

