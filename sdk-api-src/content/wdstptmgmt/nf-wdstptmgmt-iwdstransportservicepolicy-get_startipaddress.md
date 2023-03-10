---
UID: NF:wdstptmgmt.IWdsTransportServicePolicy.get_StartIpAddress
title: IWdsTransportServicePolicy::get_StartIpAddress (wdstptmgmt.h)
description: Enables a WDS client computer to configure the start of a multicast IP address range for a specified type of IP address. (Get)
helpviewer_keywords: ["IWdsTransportServicePolicy interface [Windows Deployment Services]","StartIpAddress property","IWdsTransportServicePolicy.StartIpAddress","IWdsTransportServicePolicy.get_StartIpAddress","IWdsTransportServicePolicy::StartIpAddress","IWdsTransportServicePolicy::get_StartIpAddress","IWdsTransportServicePolicy::put_StartIpAddress","StartIpAddress property [Windows Deployment Services]","StartIpAddress property [Windows Deployment Services]","IWdsTransportServicePolicy interface","get_StartIpAddress","wds.iwdstransportservicepolicy_startipaddress","wdstptmgmt/IWdsTransportServicePolicy::StartIpAddress","wdstptmgmt/IWdsTransportServicePolicy::get_StartIpAddress","wdstptmgmt/IWdsTransportServicePolicy::put_StartIpAddress"]
old-location: wds\iwdstransportservicepolicy_startipaddress.htm
tech.root: wds
ms.assetid: 2ff25e3f-15a4-4dc2-b383-ca9027a650da
ms.date: 12/05/2018
ms.keywords: IWdsTransportServicePolicy interface [Windows Deployment Services],StartIpAddress property, IWdsTransportServicePolicy.StartIpAddress, IWdsTransportServicePolicy.get_StartIpAddress, IWdsTransportServicePolicy::StartIpAddress, IWdsTransportServicePolicy::get_StartIpAddress, IWdsTransportServicePolicy::put_StartIpAddress, StartIpAddress property [Windows Deployment Services], StartIpAddress property [Windows Deployment Services],IWdsTransportServicePolicy interface, get_StartIpAddress, wds.iwdstransportservicepolicy_startipaddress, wdstptmgmt/IWdsTransportServicePolicy::StartIpAddress, wdstptmgmt/IWdsTransportServicePolicy::get_StartIpAddress, wdstptmgmt/IWdsTransportServicePolicy::put_StartIpAddress
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
 - IWdsTransportServicePolicy::get_StartIpAddress
 - wdstptmgmt/IWdsTransportServicePolicy::get_StartIpAddress
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
 - IWdsTransportServicePolicy.StartIpAddress
 - IWdsTransportServicePolicy.get_StartIpAddress
 - IWdsTransportServicePolicy.put_StartIpAddress
---

# IWdsTransportServicePolicy::get_StartIpAddress


## -description

Enables a WDS client computer to configure the start of a multicast IP address range for a specified type of IP address.

This property is read/write.

## -parameters

## -remarks

When setting the start IP address, this property validates that it is a valid multicast IP address for the specified type of IP address.

## -see-also

<a href="/windows/desktop/api/wdstptmgmt/nn-wdstptmgmt-iwdstransportservicepolicy">IWdsTransportServicePolicy</a>



<a href="/windows/win32/api/wdstptmgmt/ne-wdstptmgmt-wdstransport_ip_address_type">WDSTRANSPORT_IP_ADDRESS_TYPE</a>
