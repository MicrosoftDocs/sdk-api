---
UID: NF:wtsprotocol.IWRdsProtocolLicenseConnection.ProtocolComplete
title: IWRdsProtocolLicenseConnection::ProtocolComplete
author: windows-sdk-content
description: Notifies the protocol whether the licensing process completed successfully.
old-location: termserv\iwrdsprotocollicenseconnection_protocolcomplete.htm
tech.root: TermServ
ms.assetid: d9b0efe8-2988-4797-921a-544f410ac6d0
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IWRdsProtocolLicenseConnection interface [Remote Desktop Services],ProtocolComplete method, IWRdsProtocolLicenseConnection.ProtocolComplete, IWRdsProtocolLicenseConnection::ProtocolComplete, ProtocolComplete, ProtocolComplete method [Remote Desktop Services], ProtocolComplete method [Remote Desktop Services],IWRdsProtocolLicenseConnection interface, termserv.iwrdsprotocollicenseconnection_protocolcomplete, wtsprotocol/IWRdsProtocolLicenseConnection::ProtocolComplete
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
 - IWRdsProtocolLicenseConnection.ProtocolComplete
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWRdsProtocolLicenseConnection::ProtocolComplete


## -description


Notifies the protocol whether the licensing process completed successfully.


## -parameters




### -param ulComplete [in]

An integer that specifies whether the licensing process ended successfully. A value of 1 means success. All other values indicate failure.


## -returns



When you are implementing this method, return <b>S_OK</b> if the function succeeds. If it fails, return an <b>HRESULT</b> value that indicates the error. For a list of common error codes, see <a href="https://msdn.microsoft.com/ce52efc3-92c7-40e4-ac49-0c54049e169f">Common HRESULT Values</a>. 




## -see-also




<a href="https://msdn.microsoft.com/498c31c5-1cb6-41d7-91fb-7409ea03dda0">IWRdsProtocolLicenseConnection</a>
 

 

