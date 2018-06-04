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

# _SECURITY_QUALITY_OF_SERVICE structure


## -description


The <b>SECURITY_QUALITY_OF_SERVICE</b> data structure contains information used to support client impersonation. A client can specify this information when it connects to a server; the information determines whether the server may impersonate the client, and if so, to what extent.


## -struct-fields




### -field Length

Specifies the size, in bytes, of this structure.


### -field ImpersonationLevel

Specifies the information given to the server about the client, and how the server may represent, or impersonate, the client. Security impersonation levels govern the degree to which a server process can act on behalf of a client <a href="https://msdn.microsoft.com/library/windows/hardware/dn756307">process</a>. This member is a 
<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a> enumeration type value.


### -field ContextTrackingMode

Specifies whether the server is to be given a snapshot of the client's <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security context</a> (called static tracking), or is to be continually updated to track changes to the client's security context (called dynamic tracking). The SECURITY_STATIC_TRACKING value  specifies static tracking, and the SECURITY_DYNAMIC_TRACKING value specifies dynamic tracking. Not all communications mechanisms support dynamic tracking; those that do not will default to static tracking.


### -field EffectiveOnly

Specifies whether the server may enable or disable <a href="https://msdn.microsoft.com/library/windows/hardware/ff559863">privileges</a> and groups that the client's security context may include.


## -see-also




<a href="_win32_ddesetqualityofservice_cpp">DdeSetQualityOfService</a>



<a href="https://msdn.microsoft.com/library/windows/hardware/ff556631">SECURITY_IMPERSONATION_LEVEL</a>
 

 

