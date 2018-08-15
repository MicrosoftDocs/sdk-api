---
UID: NF:wdstptmgmt.IWdsTransportServicePolicy.get_StartIpAddress
title: IWdsTransportServicePolicy::get_StartIpAddress
author: windows-sdk-content
description: Enables a WDS client computer to configure the start of a multicast IP address range for a specified type of IP address.
old-location: wds\iwdstransportservicepolicy_startipaddress.htm
old-project: wds
ms.assetid: 2ff25e3f-15a4-4dc2-b383-ca9027a650da
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IWdsTransportServicePolicy interface [Windows Deployment Services],StartIpAddress property, IWdsTransportServicePolicy.StartIpAddress, IWdsTransportServicePolicy.get_StartIpAddress, IWdsTransportServicePolicy::StartIpAddress, IWdsTransportServicePolicy::get_StartIpAddress, IWdsTransportServicePolicy::put_StartIpAddress, StartIpAddress property [Windows Deployment Services], StartIpAddress property [Windows Deployment Services],IWdsTransportServicePolicy interface, get_StartIpAddress, wds.iwdstransportservicepolicy_startipaddress, wdstptmgmt/IWdsTransportServicePolicy::StartIpAddress, wdstptmgmt/IWdsTransportServicePolicy::get_StartIpAddress, wdstptmgmt/IWdsTransportServicePolicy::put_StartIpAddress
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wdstptmgmt.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: WDSTRANSPORT_TFTP_CAPABILITY, *PWDSTRANSPORT_TFTP_CAPABILITY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Wdstptmgmt.dll
api_name:
 - IWdsTransportServicePolicy.StartIpAddress
 - IWdsTransportServicePolicy.get_StartIpAddress
 - IWdsTransportServicePolicy.put_StartIpAddress
product: Windows
targetos: Windows
req.lib: 
req.dll: Wdstptmgmt.dll
req.irql: 
req.product: Windows Address Book 5.0
---

# IWdsTransportServicePolicy::get_StartIpAddress


## -description


Enables a WDS client computer to configure the start of a multicast IP address range for a specified type of IP address.

This property is read/write.


## -parameters


## -remarks



When setting the start IP address, this property validates that it is a valid multicast IP address for the specified type of IP address. 




## -see-also




<a href="https://msdn.microsoft.com/0a522633-87da-426c-9778-30949257e931">IWdsTransportServicePolicy</a>



<a href="https://msdn.microsoft.com/11ed1cff-eeb6-41ab-86a1-af2db5b8e155">WDSTRANSPORT_IP_ADDRESS_TYPE</a>
 

 

