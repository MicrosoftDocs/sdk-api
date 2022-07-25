---
UID: NN:netcon.INetSharingPortMapping
title: INetSharingPortMapping (netcon.h)
description: The INetSharingPortMapping interface provides methods for managing a particular port mapping.
helpviewer_keywords: ["INetSharingPortMapping","INetSharingPortMapping interface [ICS/ICF]","INetSharingPortMapping interface [ICS/ICF]","described","_ics_inetsharingportmapping","ics.inetsharingportmapping","netcon/INetSharingPortMapping"]
old-location: ics\inetsharingportmapping.htm
tech.root: ics
ms.assetid: 236608c3-061e-4db0-96df-25d263b6463b
ms.date: 12/05/2018
ms.keywords: INetSharingPortMapping, INetSharingPortMapping interface [ICS/ICF], INetSharingPortMapping interface [ICS/ICF],described, _ics_inetsharingportmapping, ics.inetsharingportmapping, netcon/INetSharingPortMapping
req.header: netcon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Hnetcfg.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INetSharingPortMapping
 - netcon/INetSharingPortMapping
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Hnetcfg.dll
api_name:
 - INetSharingPortMapping
---

# INetSharingPortMapping interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingPortMapping</b> interface provides methods for managing a particular port mapping.

## -inheritance

The <b>INetSharingPortMapping</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingPortMapping</b> also has these types of members:

## -remarks

Use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a> and 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> methods to obtain 
<b>INetSharingPortMapping</b> interfaces.

## -see-also

<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-addportmapping">INetSharingConfiguration::AddPortMapping</a>



<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
