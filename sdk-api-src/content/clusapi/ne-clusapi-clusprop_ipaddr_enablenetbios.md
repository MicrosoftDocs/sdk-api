---
UID: NE:clusapi.CLUSPROP_IPADDR_ENABLENETBIOS
title: CLUSPROP_IPADDR_ENABLENETBIOS
author: windows-sdk-content
description: When used with the CLUSPROP_DWORD structure, enables or disables the functionality of the EnableNetBIOS property of IP Address&#32;resources.
old-location: mscs\clusprop_ipaddr_enablenetbios.htm
tech.root: MsCS
ms.assetid: 4d1610f0-6a7c-4dfa-9fec-4165f28dd7de
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: CLUSPROP_IPADDR_ENABLENETBIOS, CLUSPROP_IPADDR_ENABLENETBIOS enumeration [Failover Cluster], CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED, CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED, CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED, clusapi/CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC, mscs.clusprop_ipaddr_enablenetbios
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: enum
req.header: clusapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 Enterprise, Windows Server 2008 Datacenter
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
 - ClusAPI.h
api_name:
 - CLUSPROP_IPADDR_ENABLENETBIOS
product: Windows
targetos: Windows
req.typenames: CLUSPROP_IPADDR_ENABLENETBIOS
req.redist: 
---

# CLUSPROP_IPADDR_ENABLENETBIOS enumeration


## -description


When used with the <a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a> structure, 
    enables or disables the functionality of the 
    <a href="https://msdn.microsoft.com/en-us/library/Aa370486(v=VS.85).aspx">EnableNetBIOS</a> property of 
    <a href="https://msdn.microsoft.com/en-us/library/Aa370484(v=VS.85).aspx">IP Address</a> <a href="https://msdn.microsoft.com/en-us/library/Aa372152(v=VS.85).aspx">resources</a>.


## -enum-fields




### -field CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED

Disable the functionality of the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370486(v=VS.85).aspx">EnableNetBIOS</a> property.


### -field CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED

Enable the functionality of the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370486(v=VS.85).aspx">EnableNetBIOS</a> property.


### -field CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC

Enable the functionality of the 
       <a href="https://msdn.microsoft.com/en-us/library/Aa370486(v=VS.85).aspx">EnableNetBIOS</a> property if the NIC to 
       which the IP Address resource is bound has enabled NetBIOS.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa370486(v=VS.85).aspx">EnableNetBIOS</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

