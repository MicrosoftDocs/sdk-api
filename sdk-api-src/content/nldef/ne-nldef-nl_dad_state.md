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

# NL_DAD_STATE enumeration


## -description


The <b>IP_DAD_STATE</b> enumeration specifies information about the duplicate address detection (DAD) state for an IPv4 or IPv6 address.


## -enum-fields




### -field NldsInvalid


### -field NldsTentative


### -field NldsDuplicate


### -field NldsDeprecated


### -field NldsPreferred


### -field IpDadStateInvalid

The DAD state is invalid.


### -field IpDadStateTentative

The DAD state is tentative.


### -field IpDadStateDuplicate

A duplicate IP address has been detected.


### -field IpDadStateDeprecated

The IP address has been deprecated.


### -field IpDadStatePreferred

The IP address is the preferred address.


## -remarks



The <b>IP_DAD_STATE</b> enumeration is used in the <b>DadState</b> member of the <a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a>  structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>IP_DAD_STATE</b> enumeration is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file. The  <i>Nldef.h</i> and <i>Iptypes.h</i> header files should never be used directly.




## -see-also




<a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a>
 

 

