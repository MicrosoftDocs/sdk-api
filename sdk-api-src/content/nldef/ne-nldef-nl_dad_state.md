---
UID: NE:nldef.NL_DAD_STATE
title: NL_DAD_STATE
author: windows-driver-content
description: The IP_DAD_STATE enumeration specifies information about the duplicate address detection (DAD) state for an IPv4 or IPv6 address.
old-location: iphlp\ip_dad_state.htm
old-project: IpHlp
ms.assetid: 2c67215c-6349-418e-9004-b869d6f5baef
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: IP_DAD_STATE, IP_DAD_STATE enumeration [IP Helper], IpDadStateDeprecated, IpDadStateDuplicate, IpDadStateInvalid, IpDadStatePreferred, IpDadStateTentative, NL_DAD_STATE, iphlp.ip_dad_state, iptypes/IP_DAD_STATE, iptypes/IpDadStateDeprecated, iptypes/IpDadStateDuplicate, iptypes/IpDadStateInvalid, iptypes/IpDadStatePreferred, iptypes/IpDadStateTentative, nldef/IP_DAD_STATE, nldef/IpDadStateDeprecated, nldef/IpDadStateDuplicate, nldef/IpDadStateInvalid, nldef/IpDadStatePreferred, nldef/IpDadStateTentative
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: nldef.h
req.include-header: Windows 8, Windows Server 2008 R2, Windows 7, Windows Server 2008  Windows Vista, Iphlpapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: NL_DAD_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Nldef.h
-	Iptypes.h
api_name:
-	IP_DAD_STATE
product: Windows
targetos: Windows
req.lib: Newdev.lib
req.dll: Newdev.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
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
 

 

