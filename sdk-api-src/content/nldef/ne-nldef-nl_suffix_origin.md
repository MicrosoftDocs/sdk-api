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

# NL_SUFFIX_ORIGIN enumeration


## -description


The <b>IP_SUFFIX_ORIGIN</b> enumeration specifies the origin of an IPv4 or IPv6  address suffix, and is used with the <a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a> structure.


## -enum-fields




### -field NlsoOther


### -field NlsoManual


### -field NlsoWellKnown


### -field NlsoDhcp


### -field NlsoLinkLayerAddress


### -field NlsoRandom


### -field IpSuffixOriginOther

The IP address suffix was provided by a source other than those defined in this enumeration.


### -field IpSuffixOriginManual

The IP address suffix was manually specified.


### -field IpSuffixOriginWellKnown

The IP address suffix is from a well-known source.


### -field IpSuffixOriginDhcp

The IP address suffix was provided by DHCP settings.


### -field IpSuffixOriginLinkLayerAddress

The IP address suffix was obtained from the link-layer address.


### -field IpSuffixOriginRandom

The IP address suffix was obtained from a random source.


### -field IpSuffixOriginUnchanged

The IP address suffix should be unchanged. This value is used when setting the properties for a unicast IP interface when the value for the IP suffix origin should be left unchanged.



<div class="alert"><b>Note</b>  This enumeration value is only available on Windows Vista and later.</div>
<div> </div>

## -remarks



The <b>IP_SUFFIX_ORIGIN</b> enumeration is used in the <b>SuffixOrigin</b> member of the <a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a>  structure.

On the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later, the organization of header files has changed and the <b>IP_SUFFIX_ORIGIN</b> enumeration is defined in the <i>Nldef.h</i> header file which is automatically included by the <i>Iptypes.h</i> header file. In order to use the <b>IP_SUFFIX_ORIGIN</b> enumeration, the <i>Winsock2.h</i> header file must be included before the <i>Iptypes.h</i> header file.  




## -see-also




<a href="https://msdn.microsoft.com/65c3648c-89bd-417b-8a9b-feefa6149c4a">IP_ADAPTER_UNICAST_ADDRESS</a>
 

 

