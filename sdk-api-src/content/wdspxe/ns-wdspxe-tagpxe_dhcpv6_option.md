---
UID: NS:wdspxe.tagPXE_DHCPV6_OPTION
title: tagPXE_DHCPV6_OPTION
author: windows-sdk-content
description: The PXE_DHCPV6_OPTION structure can be used with the Windows Deployment Services PXE Server API.
old-location: wds\pxe_dhcpv6_option.htm
old-project: Wds
ms.assetid: 9B0A1A5B-1CF7-46B4-9C94-42355555DD60
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PPXE_DHCPV6_OPTION, PPXE_DHCPV6_OPTION, PPXE_DHCPV6_OPTION structure pointer [Windows Deployment Services], PXE_DHCPV6_OPTION, PXE_DHCPV6_OPTION structure [Windows Deployment Services], tagPXE_DHCPV6_OPTION, wds.pxe_dhcpv6_option, wdspxe/PPXE_DHCPV6_OPTION, wdspxe/PXE_DHCPV6_OPTION"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wdspxe.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
req.typenames: PXE_DHCPV6_OPTION, *PPXE_DHCPV6_OPTION
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - WdsPxe.h
api_name:
 - PXE_DHCPV6_OPTION
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# tagPXE_DHCPV6_OPTION structure


## -description


The <b>PXE_DHCPV6_OPTION</b> structure can be used with the Windows Deployment Services PXE Server API. 

For more information about the DHCPv6 option code, developers should refer to the Dynamic Host Configuration Protocol for IPv6 (<a href="Http://go.microsoft.com/fwlink/p/?linkid=132626">RFC 3315</a>) maintained by The Internet Engineering Task Force (IETF).


## -struct-fields




### -field OptionCode

A DHCPv6 option type.


### -field DataLength

Length of the option value.


### -field Data

The option value.

