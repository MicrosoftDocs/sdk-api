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

# CLUSPROP_IPADDR_ENABLENETBIOS enumeration


## -description


When used with the <a href="https://msdn.microsoft.com/96d81777-be45-4dbb-8426-f68cb51e2a42">CLUSPROP_DWORD</a> structure, 
    enables or disables the functionality of the 
    <a href="https://msdn.microsoft.com/7b767335-edc1-47d7-8dea-13f6df902e5e">EnableNetBIOS</a> property of 
    <a href="https://msdn.microsoft.com/3ed966f1-0177-4376-a36d-4a2fda327470">IP Address</a> <a href="https://msdn.microsoft.com/090d1c20-fab3-43dd-bfe2-a2c3f9ba8f89">resources</a>.


## -enum-fields




### -field CLUSPROP_IPADDR_ENABLENETBIOS_DISABLED

Disable the functionality of the 
       <a href="https://msdn.microsoft.com/7b767335-edc1-47d7-8dea-13f6df902e5e">EnableNetBIOS</a> property.


### -field CLUSPROP_IPADDR_ENABLENETBIOS_ENABLED

Enable the functionality of the 
       <a href="https://msdn.microsoft.com/7b767335-edc1-47d7-8dea-13f6df902e5e">EnableNetBIOS</a> property.


### -field CLUSPROP_IPADDR_ENABLENETBIOS_TRACK_NIC

Enable the functionality of the 
       <a href="https://msdn.microsoft.com/7b767335-edc1-47d7-8dea-13f6df902e5e">EnableNetBIOS</a> property if the NIC to 
       which the IP Address resource is bound has enabled NetBIOS.


## -see-also




<a href="https://msdn.microsoft.com/7b767335-edc1-47d7-8dea-13f6df902e5e">EnableNetBIOS</a>



<a href="https://msdn.microsoft.com/546071de-1067-4b47-b862-668be976e563">Failover Cluster Enumerations</a>
 

 

