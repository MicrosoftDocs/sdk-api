---
UID: NF:wdstptmgmt.IWdsTransportServicePolicy.put_EndIpAddress
title: IWdsTransportServicePolicy::put_EndIpAddress (wdstptmgmt.h)
description: Enables a WDS client computer to configure the end of a multicast IP address range for a specified type of IP address. (Put)
helpviewer_keywords: ["EndIpAddress property [Windows Deployment Services]","EndIpAddress property [Windows Deployment Services]","IWdsTransportServicePolicy interface","IWdsTransportServicePolicy interface [Windows Deployment Services]","EndIpAddress property","IWdsTransportServicePolicy.EndIpAddress","IWdsTransportServicePolicy.put_EndIpAddress","IWdsTransportServicePolicy::EndIpAddress","IWdsTransportServicePolicy::get_EndIpAddress","IWdsTransportServicePolicy::put_EndIpAddress","put_EndIpAddress","wds.iwdstransportservicepolicy_endipaddress","wdstptmgmt/IWdsTransportServicePolicy::EndIpAddress","wdstptmgmt/IWdsTransportServicePolicy::get_EndIpAddress","wdstptmgmt/IWdsTransportServicePolicy::put_EndIpAddress"]
old-location: wds\iwdstransportservicepolicy_endipaddress.htm
tech.root: wds
ms.assetid: 9900acb3-a66b-4279-becc-6ad1a040d534
ms.date: 12/05/2018
ms.keywords: EndIpAddress property [Windows Deployment Services], EndIpAddress property [Windows Deployment Services],IWdsTransportServicePolicy interface, IWdsTransportServicePolicy interface [Windows Deployment Services],EndIpAddress property, IWdsTransportServicePolicy.EndIpAddress, IWdsTransportServicePolicy.put_EndIpAddress, IWdsTransportServicePolicy::EndIpAddress, IWdsTransportServicePolicy::get_EndIpAddress, IWdsTransportServicePolicy::put_EndIpAddress, put_EndIpAddress, wds.iwdstransportservicepolicy_endipaddress, wdstptmgmt/IWdsTransportServicePolicy::EndIpAddress, wdstptmgmt/IWdsTransportServicePolicy::get_EndIpAddress, wdstptmgmt/IWdsTransportServicePolicy::put_EndIpAddress
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IWdsTransportServicePolicy::put_EndIpAddress
 - wdstptmgmt/IWdsTransportServicePolicy::put_EndIpAddress
dev_langs:
 - c++
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
---

# IWdsTransportServicePolicy::put_EndIpAddress


## -description

Enables a WDS client computer to configure the end of a multicast IP address range for a specified type of IP address. 

This property is read/write.

## -parameters

## -remarks

When setting the end IP address, this property validates that it is a valid multicast IP address for the specified type of IP address.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportservicepolicy">IWdsTransportServicePolicy</a>



<a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_ip_address_type">WDSTRANSPORT_IP_ADDRESS_TYPE</a>
