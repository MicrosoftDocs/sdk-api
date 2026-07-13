---
UID: NN:bdaiface.IBDA_EthernetFilter
title: IBDA_EthernetFilter (bdaiface.h)
description: The IBDA_EthernetFilter interface is implemented on a Network Provider.
helpviewer_keywords: ["IBDA_EthernetFilter","IBDA_EthernetFilter interface [Microsoft TV Technologies]","IBDA_EthernetFilter interface [Microsoft TV Technologies]","described","IBDA_EthernetFilterInterface","bdaiface/IBDA_EthernetFilter","mstv.ibda_ethernetfilter"]
old-location: mstv\ibda_ethernetfilter.htm
tech.root: mstv
ms.assetid: f4f9d6c0-0acf-416b-adb3-643ac0167d0a
ms.date: 12/05/2018
ms.keywords: IBDA_EthernetFilter, IBDA_EthernetFilter interface [Microsoft TV Technologies], IBDA_EthernetFilter interface [Microsoft TV Technologies],described, IBDA_EthernetFilterInterface, bdaiface/IBDA_EthernetFilter, mstv.ibda_ethernetfilter
req.header: bdaiface.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBDA_EthernetFilter
 - bdaiface/IBDA_EthernetFilter
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - bdaiface.h
api_name:
 - IBDA_EthernetFilter
---

# IBDA_EthernetFilter interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_EthernetFilter</b> interface is implemented on a Network Provider. The methods are called by the BDA IPSink filter in order to give the Network Provider a list of multicast Ethernet addresses being requested by an application. The Network Provider then informs all registered transport information filters (TIFs) of the new addresses. The TIF(s) are responsible for mapping those addresses to PIDs and passing the PIDs back to the Network Provider, which then resets the PID list for the IP data output pin on the MPEG-2 Demultiplexer. This causes the IP data on the specified PIDs to be routed through the data services segment of the graph and on to Winsock where the listening application can receive it. The <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipv4filter">IBDA_IPV4Filter</a> interface performs the same function for IPv4 multicast addresses.

## -inheritance

The <b>IBDA_EthernetFilter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_EthernetFilter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_EthernetFilter)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
