---
UID: NF:wdstptmgmt.IWdsTransportServicePolicy.get_EndIpAddress
title: IWdsTransportServicePolicy::get_EndIpAddress
author: windows-sdk-content
description: Enables a WDS client computer to configure the end of a multicast IP address range for a specified type of IP address.
old-location: wds\iwdstransportservicepolicy_endipaddress.htm
tech.root: wds
ms.assetid: 9900acb3-a66b-4279-becc-6ad1a040d534
ms.author: windowssdkdev
ms.date: 09/14/2018
ms.keywords: EndIpAddress property [Windows Deployment Services], EndIpAddress property [Windows Deployment Services],IWdsTransportServicePolicy interface, IWdsTransportServicePolicy interface [Windows Deployment Services],EndIpAddress property, IWdsTransportServicePolicy.EndIpAddress, IWdsTransportServicePolicy.get_EndIpAddress, IWdsTransportServicePolicy::EndIpAddress, IWdsTransportServicePolicy::get_EndIpAddress, IWdsTransportServicePolicy::put_EndIpAddress, get_EndIpAddress, wds.iwdstransportservicepolicy_endipaddress, wdstptmgmt/IWdsTransportServicePolicy::EndIpAddress, wdstptmgmt/IWdsTransportServicePolicy::get_EndIpAddress, wdstptmgmt/IWdsTransportServicePolicy::put_EndIpAddress
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wdstptmgmt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: Wdstptmgmt.tlb
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportServicePolicy.EndIpAddress
 - IWdsTransportServicePolicy.get_EndIpAddress
 - IWdsTransportServicePolicy.put_EndIpAddress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWdsTransportServicePolicy::get_EndIpAddress


## -description


Enables a WDS client computer to configure the end of a multicast IP address range for a specified type of IP address. 

This property is read/write.


## -parameters


## -remarks



When setting the end IP address, this property validates that it is a valid multicast IP address for the specified type of IP address. 




## -see-also




<a href="https://msdn.microsoft.com/0a522633-87da-426c-9778-30949257e931">IWdsTransportServicePolicy</a>



<a href="https://msdn.microsoft.com/11ed1cff-eeb6-41ab-86a1-af2db5b8e155">WDSTRANSPORT_IP_ADDRESS_TYPE</a>
 

 

