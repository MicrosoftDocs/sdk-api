---
UID: NF:wtsprotocol.IWTSProtocolLicenseConnection.ProtocolComplete
title: IWTSProtocolLicenseConnection::ProtocolComplete
author: windows-sdk-content
description: IWTSProtocolLicenseConnection::ProtocolComplete is no longer available. Instead, use IWRdsProtocolLicenseConnection::ProtocolComplete.
old-location: termserv\iwtsprotocollicenseconnection_protocolcomplete.htm
old-project: TermServ
ms.assetid: 3a615e25-51d0-49eb-ae0f-185fd3a0ea23
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: IWTSProtocolLicenseConnection interface [Remote Desktop Services],ProtocolComplete method, IWTSProtocolLicenseConnection.ProtocolComplete, IWTSProtocolLicenseConnection::ProtocolComplete, ProtocolComplete, ProtocolComplete method [Remote Desktop Services], ProtocolComplete method [Remote Desktop Services],IWTSProtocolLicenseConnection interface, termserv.iwtsprotocollicenseconnection_protocolcomplete, wtsprotocol/IWTSProtocolLicenseConnection::ProtocolComplete
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: WTS_PROPERTY_VALUE, *PWTS_PROPERTY_VALUE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wtsprotocol.h
api_name:
 - IWTSProtocolLicenseConnection.ProtocolComplete
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWTSProtocolLicenseConnection::ProtocolComplete


## -description


<p class="CCE_Message">[<b>IWTSProtocolLicenseConnection::ProtocolComplete</b> is no longer available for use as of Windows Server 2012. Instead, use <a href="https://msdn.microsoft.com/d9b0efe8-2988-4797-921a-544f410ac6d0">IWRdsProtocolLicenseConnection::ProtocolComplete</a>.]

Notifies the protocol whether the licensing process completed successfully.


## -parameters




### -param ulComplete [in]

An integer that specifies whether the licensing process ended successfully. A value of one (1) means success. All other values indicate failure.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/3f6925b6-c712-40c6-8b48-7df8ef4a9872">IWTSProtocolLicenseConnection</a>
 

 

