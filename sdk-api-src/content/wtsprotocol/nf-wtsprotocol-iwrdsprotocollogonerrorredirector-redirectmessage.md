---
UID: NF:wtsprotocol.IWRdsProtocolLogonErrorRedirector.RedirectMessage
title: IWRdsProtocolLogonErrorRedirector::RedirectMessage
author: windows-sdk-content
description: Queries the protocol regarding how to redirect the logon message.
old-location: termserv\iwrdsprotocollogonerrorredirector_redirectmessage.htm
tech.root: termserv
ms.assetid: b818e2b0-3d6c-4a56-8175-75b585553520
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWRdsProtocolLogonErrorRedirector interface [Remote Desktop Services],RedirectMessage method, IWRdsProtocolLogonErrorRedirector.RedirectMessage, IWRdsProtocolLogonErrorRedirector::RedirectMessage, RedirectMessage, RedirectMessage method [Remote Desktop Services], RedirectMessage method [Remote Desktop Services],IWRdsProtocolLogonErrorRedirector interface, termserv.iwrdsprotocollogonerrorredirector_redirectmessage, wtsprotocol/IWRdsProtocolLogonErrorRedirector::RedirectMessage
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wtsprotocol.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012
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
 - wtsprotocol.h
api_name:
 - IWRdsProtocolLogonErrorRedirector.RedirectMessage
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolLogonErrorRedirector::RedirectMessage


## -description


Queries the protocol regarding how to redirect the logon message.


## -parameters




### -param pszCaption [in]

A pointer to a string that contains the message box caption.


### -param pszMessage [in]

A pointer to a string that contains the logon message.


### -param uType [in]

An integer that contains the message box type. For more information, see the <a href="https://msdn.microsoft.com/en-us/library/ms645505(v=VS.85).aspx">MessageBox</a> function.


### -param pResponse [out]

A pointer to a <a href="https://msdn.microsoft.com/67ed8d6f-641c-4739-911c-e61379e14048">WRDS_LOGON_ERROR_REDIRECTOR_RESPONSE</a> enumeration that specifies to the Remote Desktop Services service the preferred response for redirecting the logon message.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>.




## -see-also




<a href="https://msdn.microsoft.com/43c283f5-c902-49cc-81a0-15fc6316c7d4">IWRdsProtocolLogonErrorRedirector</a>
 

 

