---
UID: NN:netcon.INetSharingManager
title: INetSharingManager (netcon.h)
description: The INetSharingManager interface is the primary interface for the Manager object. INetSharingManager provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.
helpviewer_keywords: ["INetSharingManager","INetSharingManager interface [ICS/ICF]","INetSharingManager interface [ICS/ICF]","described","_ics_inetsharingmanager","ics.inetsharingmanager","netcon/INetSharingManager"]
old-location: ics\inetsharingmanager.htm
tech.root: ics
ms.assetid: e7009d13-89c2-4fd9-8f6c-dcdc67178598
ms.date: 12/05/2018
ms.keywords: INetSharingManager, INetSharingManager interface [ICS/ICF], INetSharingManager interface [ICS/ICF],described, _ics_inetsharingmanager, ics.inetsharingmanager, netcon/INetSharingManager
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
 - INetSharingManager
 - netcon/INetSharingManager
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
 - INetSharingManager
---

# INetSharingManager interface


## -description

<p class="CCE_Message">[Internet Connection Firewall may be altered or unavailable in subsequent versions. Instead, use the <a href="/previous-versions/windows/desktop/ics/windows-firewall-start-page">Windows Firewall API</a>.]

The 
<b>INetSharingManager</b> interface is the primary interface for the Manager object. 
<b>INetSharingManager</b> provides methods to determine if sharing is installed, to manage port mappings, and to obtain enumeration interfaces for public and private connections.

## -inheritance

The <b>INetSharingManager</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>INetSharingManager</b> also has these types of members:

## -remarks

To obtain an enumeration interface for port mappings, use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingmanager-get_inetsharingconfigurationforinetconnection">get_INetSharingConfigurationForINetConnection</a> method to obtain an 
<a href="/previous-versions/windows/desktop/api/netcon/nn-netcon-inetsharingconfiguration">INetSharingConfiguration</a> interface. Then use the 
<a href="/previous-versions/windows/desktop/api/netcon/nf-netcon-inetsharingconfiguration-get_enumportmappings">INetSharingConfiguration::EnumPortMappings</a> method to obtain an 
<a href="/windows/desktop/api/netcon/nn-netcon-ienumnetsharingportmapping">IEnumNetSharingPortMapping</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-interfaces">Internet Connection Sharing and Internet Connection Firewall Interfaces</a>



<a href="/previous-versions/windows/desktop/ics/internet-connection-sharing-and-internet-connection-firewall-reference">Internet Connection Sharing and Internet Connection Firewall Reference</a>
