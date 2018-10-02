---
UID: NF:wtsprotocol.IWTSProtocolLogonErrorRedirector.OnBeginPainting
title: IWTSProtocolLogonErrorRedirector::OnBeginPainting
author: windows-sdk-content
description: IWTSProtocolLogonErrorRedirector::OnBeginPainting is no longer available. Instead, use IWRdsProtocolLogonErrorRedirector::OnBeginPainting.
old-location: termserv\iwtsprotocollogonerrorredirector_onbeginpainting.htm
tech.root: TermServ
ms.assetid: 1356deeb-ac4a-4877-95be-9df09f4b0210
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IWTSProtocolLogonErrorRedirector interface [Remote Desktop Services],OnBeginPainting method, IWTSProtocolLogonErrorRedirector.OnBeginPainting, IWTSProtocolLogonErrorRedirector::OnBeginPainting, OnBeginPainting, OnBeginPainting method [Remote Desktop Services], OnBeginPainting method [Remote Desktop Services],IWTSProtocolLogonErrorRedirector interface, termserv.iwtsprotocollogonerrorredirector_onbeginpainting, wtsprotocol/IWTSProtocolLogonErrorRedirector::OnBeginPainting
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Wtsprotocol.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLogonErrorRedirector.OnBeginPainting
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWTSProtocolLogonErrorRedirector::OnBeginPainting


## -description


<p class="CCE_Message">[<b>IWTSProtocolLogonErrorRedirector::OnBeginPainting</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/cc044746-1127-44a3-993d-ca2445c99ff6">IWRdsProtocolLogonErrorRedirector::OnBeginPainting</a>.]

Notifies the protocol that the logon user interface is ready to begin painting.


## -parameters






## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/1ff30217-9091-47df-a38f-30784538f0b9">IWTSProtocolLogonErrorRedirector</a>
 

 

