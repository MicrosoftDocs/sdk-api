---
UID: NF:dhcpsapi.DhcpDeleteSubnet
title: DhcpDeleteSubnet function
author: windows-sdk-content
description: The DhcpDeleteSubnet function deletes a subnet from the DHCP server.
old-location: dhcp\dhcpdeletesubnet.htm
tech.root: DHCP
ms.assetid: e000a81b-b61b-4ba9-adee-4940edc78050
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DhcpDeleteSubnet, DhcpDeleteSubnet function [DHCP], dhcp.dhcpdeletesubnet, dhcpsapi/DhcpDeleteSubnet
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpDeleteSubnet
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DhcpDeleteSubnet
: 
---

# DhcpDeleteSubnet function


## -description


The <b>DhcpDeleteSubnet</b> function deletes a subnet from the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address of the subnet to delete.


### -param SubnetAddress [in]


<a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_IP_ADDRESS</a> value that contains the IP address of the subnet gateway used to identify the subnet.


### -param ForceFlag [in]


<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b">DHCP_FORCE_FLAG</a> enumeration value that indicates the type of delete operation to perform (full force, failover force, or no force).


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -remarks



Usually, you will use either <b>DhcpFullForce</b> or <b>DhcpNoForce</b> as the value for <i>ForceFlag</i>. The <b>DhcpFailoverForce</b> value is intended for use when cleaning up a broken or improperly configured DHCP failover configuration. In that case, use of <b>DhcpFailoverForce</b> ensures that the entire DNS configuration isn't improperly deleted while cleaning up the DHCP failover configuration. Note that the minimum server OS requirement for <b>DhcpFailoverForce</b> is Windows Server 2012 R2 with KB 3100473 installed.




## -see-also




<a href="https://msdn.microsoft.com/2ec45a99-432d-4218-9048-81714ceff36b"> DHCP_FORCE_FLAG</a>



<a href="https://msdn.microsoft.com/acae01cf-cbd9-4461-a1cc-5fcb745b9c8f">DhcpCreateSubnet</a>



<a href="https://msdn.microsoft.com/333381c9-66d1-44ef-911b-d543c79abefb">DhcpEnumSubnets</a>
 

 

