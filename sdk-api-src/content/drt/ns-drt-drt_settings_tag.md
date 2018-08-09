---
UID: NS:drt.drt_settings_tag
title: drt_settings_tag
author: windows-sdk-content
description: DRT_SETTINGS structure contains the settings utilized by the local Distributed Routing Table.
old-location: p2p\drt_settings.htm
old-project: p2psdk
ms.assetid: 22408b8e-b114-43cd-8f84-3eaf8508f441
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: "*PDRT_SETTINGS, DRT_SETTINGS, DRT_SETTINGS structure [Peer Networking], PDRT_SETTINGS, PDRT_SETTINGS structure pointer [Peer Networking], drt/DRT_SETTINGS, drt/PDRT_SETTINGS, drt_settings_tag, p2p.drt_settings"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: drt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 Professional [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DRT_SETTINGS, *PDRT_SETTINGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - drt.h
api_name:
 - DRT_SETTINGS
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# drt_settings_tag structure


## -description


The <b>DRT_SETTINGS</b> structure contains the settings utilized by the local Distributed Routing Table.


## -struct-fields




### -field dwSize

The size of the  structure specified by  the  <i>sizeof</i> parameter found in <b>DRT_SETTINGS</b> with the purpose of  allowing new fields in the structure in future versions of the DRT API.


### -field cbKey

Specifies the exact number of bytes for keys in this DRT instance.  Currently only 8 bytes are supported. Any other values will return <b>E_INVALIDARG</b> via the <a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a> function.


### -field bProtocolMajorVersion

Pointer to the byte array that represents the protocol major version specified by the application. This is packed in every DRT packet to identify the version of the Security or Bootstrap Providers in use when a single DRT instance is supporting multiple Security or Bootstrap Providers.


### -field bProtocolMinorVersion

Pointer to the byte array that represents the protocol minor version specified by the application. 
 This is packed in every DRT packet to identify the version of the Security or Bootstrap Providers in use when a single DRT instance is supporting multiple Security or Bootstrap Providers.


### -field ulMaxRoutingAddresses

Specifies the maximum number of address the DRT registers when an application registers a key. The maximum value for this field is 4.


### -field pwzDrtInstancePrefix

This string forms the basis of the name of the DRT instance. The name of the instance can be used to locate the Windows performance counters associated with it.


### -field hTransport

Handle to a transport created by the transport creation API.  This is used to open a DRT with a transport specified by the <b>DRT_SETTINGS</b> structure.  Currently only IPv6 UDP is supported via <a href="https://msdn.microsoft.com/def3120b-98b6-4e31-8166-822cea7fea69">DrtCreateIpv6UdpTransport</a>.


### -field pSecurityProvider

Pointer to the security provider specified for use. An instance of the Derived Key Security Provider can be obtained by calling <a href="https://msdn.microsoft.com/e4cc8326-e2bc-459f-97dd-a00cfd1ed35e">DrtCreateDerivedKeySecurityProvider</a>.


### -field pBootstrapProvider

 


### -field eSecurityMode

Specifies the security mode that the DRT should operate under. All nodes participating in a DRT mesh must use the same security mode.


#### - pBootStrapProvider

Pointer to the Bootstrap Provider specified for use. An instance of the PNRP Bootstrap Provider can be obtained by calling <a href="https://msdn.microsoft.com/5bd64f10-abb8-4cba-8ebd-780a6a0c7074">DrtCreatePnrpBootstrapResolver</a>.


## -see-also




<a href="https://msdn.microsoft.com/def3120b-98b6-4e31-8166-822cea7fea69">DrtCreateIpv6UdpTransport</a>



<a href="https://msdn.microsoft.com/5bd64f10-abb8-4cba-8ebd-780a6a0c7074">DrtCreatePnrpBootstrapResolver</a>



<a href="https://msdn.microsoft.com/67320767-f622-478a-a886-bbea1650ac1a">DrtOpen</a>
 

 

