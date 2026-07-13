---
UID: NN:netcon.IEnumNetSharingPortMapping
title: IEnumNetSharingPortMapping (netcon.h)
description: The IEnumNetSharingPortMapping interface provides methods to enumerate the port mappings for a particular connection.
helpviewer_keywords: ["IEnumNetSharingPortMapping","IEnumNetSharingPortMapping interface [ICS/ICF]","IEnumNetSharingPortMapping interface [ICS/ICF]","described","_ics_ienumnetsharingportmapping","ics.ienumnetsharingportmapping","netcon/IEnumNetSharingPortMapping"]
old-location: ics\ienumnetsharingportmapping.htm
tech.root: ics
ms.assetid: 68334bd2-353f-457d-a2c7-1271816f10f5
ms.date: 12/05/2018
ms.keywords: IEnumNetSharingPortMapping, IEnumNetSharingPortMapping interface [ICS/ICF], IEnumNetSharingPortMapping interface [ICS/ICF],described, _ics_ienumnetsharingportmapping, ics.ienumnetsharingportmapping, netcon/IEnumNetSharingPortMapping
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
 - IEnumNetSharingPortMapping
 - netcon/IEnumNetSharingPortMapping
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
 - IEnumNetSharingPortMapping
---

# IEnumNetSharingPortMapping interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>IEnumNetSharingPortMapping</b> interface provides methods to enumerate the port mappings for a particular connection.

## -inheritance

The <b>IEnumNetSharingPortMapping</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumNetSharingPortMapping</b> also has these types of members:

## -remarks

To obtain an enumeration interface for port mappings, use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">INetSharingManager::get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface. Then use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<b>IEnumNetSharingPortMapping</b> interface.

## -see-also

<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-ienumvariant">IEnumVARIANT</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
