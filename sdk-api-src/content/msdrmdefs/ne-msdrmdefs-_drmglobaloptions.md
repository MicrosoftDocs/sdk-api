---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _DRMGLOBALOPTIONS enumeration


## -description


<p class="CCE_Message">[The AD RMS SDK leveraging functionality exposed by 

the client in Msdrm.dll is available for use in Windows Server 2008, Windows Vista, Windows Server 2008 R2, Windows 7, Windows Server 2012, and Windows 8. It may be altered or 

unavailable in subsequent versions. Instead, use <a href="https://msdn.microsoft.com/a7900f40-4c53-4760-8e5a-9c88149f86d0">Active Directory Rights Management Services SDK 2.1</a>, 

which leverages functionality exposed by the client in Msipc.dll.]

The <b>DRMGLOBALOPTIONS</b> enumeration defines values for specifying which protocol is used for the transport protocol and whether the server lockbox is used. This enumeration is used by the <a href="https://msdn.microsoft.com/fff0d503-e342-4f50-810c-bda4e9e14ad7">DRMSetGlobalOptions</a> function.


## -enum-fields




### -field DRMGLOBALOPTIONS_USE_WINHTTP

The WinHTTP protocol is used for the transport protocol. By default, the WinINet protocol is used.


### -field DRMGLOBALOPTIONS_USE_SERVERSECURITYPROCESSOR

The server lockbox is used. For more information, see <a href="https://msdn.microsoft.com/d67b7326-e447-4bfa-b015-1b546b68d7e2">Lockboxes</a>.


## -remarks



Applications cannot toggle between the WinHTTP and WinINet protocols.

WinINet cannot be used under the network service account. If an application will be run under the network service account, the application must specify the <b>DRMGLOBALOPTIONS_USE_WINHTTP</b> option.




## -see-also




<a href="https://msdn.microsoft.com/bc3a8ab3-9f89-442b-9910-85820b2b2653">AD RMS Enumerations</a>



<a href="https://msdn.microsoft.com/fff0d503-e342-4f50-810c-bda4e9e14ad7">DRMSetGlobalOptions</a>
 

 

