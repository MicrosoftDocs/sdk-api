---
UID: NE:sysinfoapi._COMPUTER_NAME_FORMAT
title: "_COMPUTER_NAME_FORMAT"
author: windows-sdk-content
description: Specifies a type of computer name.
old-location: base\computer_name_format_str.htm
tech.root: sysinfo
ms.assetid: 249830be-acd7-4417-ac33-c0fb2d87c4af
ms.author: windowssdkdev
ms.date: 11/09/2018
ms.keywords: COMPUTER_NAME_FORMAT, COMPUTER_NAME_FORMAT enumeration, ComputerNameDnsDomain, ComputerNameDnsFullyQualified, ComputerNameDnsHostname, ComputerNameMax, ComputerNameNetBIOS, ComputerNamePhysicalDnsDomain, ComputerNamePhysicalDnsFullyQualified, ComputerNamePhysicalDnsHostname, ComputerNamePhysicalNetBIOS, _COMPUTER_NAME_FORMAT, _win32_computer_name_format_str, base.computer_name_format_str, sysinfoapi/COMPUTER_NAME_FORMAT, sysinfoapi/ComputerNameDnsDomain, sysinfoapi/ComputerNameDnsFullyQualified, sysinfoapi/ComputerNameDnsHostname, sysinfoapi/ComputerNameMax, sysinfoapi/ComputerNameNetBIOS, sysinfoapi/ComputerNamePhysicalDnsDomain, sysinfoapi/ComputerNamePhysicalDnsFullyQualified, sysinfoapi/ComputerNamePhysicalDnsHostname, sysinfoapi/ComputerNamePhysicalNetBIOS
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: sysinfoapi.h
req.include-header: Windows.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
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
 - HeaderDef
api_location:
 - sysinfoapi.h
api_name:
 - COMPUTER_NAME_FORMAT
product: Windows
targetos: Windows
req.typenames: COMPUTER_NAME_FORMAT
req.redist: 
---

# _COMPUTER_NAME_FORMAT enumeration


## -description


Specifies a type of computer name.


## -enum-fields




### -field ComputerNameNetBIOS

The NetBIOS name of the local computer or the cluster associated with the local computer. This name is limited to MAX_COMPUTERNAME_LENGTH + 1 characters and may be a truncated version of the DNS host name. For example, if the DNS host name is "corporate-mail-server", the NetBIOS name would be "corporate-mail-".


### -field ComputerNameDnsHostname

The DNS name of the local computer or the cluster associated with the local computer.


### -field ComputerNameDnsDomain

The name of the DNS domain assigned to the local computer or the cluster associated with the local computer.


### -field ComputerNameDnsFullyQualified

The fully qualified DNS name that uniquely identifies the local computer or the cluster associated with the local computer. 




This name is a combination of the DNS host name and the DNS domain name, using the form <i>HostName</i>.<i>DomainName</i>. For example, if the DNS host name is "corporate-mail-server" and the DNS domain name is "microsoft.com", the fully qualified DNS name is "corporate-mail-server.microsoft.com".


### -field ComputerNamePhysicalNetBIOS

The NetBIOS name of the local computer. On a cluster, this is the NetBIOS name of the local node on the cluster.


### -field ComputerNamePhysicalDnsHostname

The DNS host name of the local computer. On a cluster, this is the DNS host name of the local node on the cluster.


### -field ComputerNamePhysicalDnsDomain

The name of the DNS domain assigned to the local computer. On a cluster, this is the DNS domain of the local node on the cluster.


### -field ComputerNamePhysicalDnsFullyQualified

The fully qualified DNS name that uniquely identifies the computer. On a cluster, this is the fully qualified DNS name of the local node on the cluster. The fully qualified DNS name is a combination of the DNS host name and the DNS domain name, using the form <i>HostName</i>.<i>DomainName</i>.


### -field ComputerNameMax

Not used.


## -see-also




<a href="https://msdn.microsoft.com/eae3f75d-7ec7-42ae-b207-e3ebaa33346e">GetComputerNameEx</a>



<a href="https://msdn.microsoft.com/12163456-770c-4f9e-9261-a6ea5f2cd93a">SetComputerNameEx</a>
 

 

