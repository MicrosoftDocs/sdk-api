---
UID: NN:bdaiface.IBDA_IPV4Filter
title: IBDA_IPV4Filter (bdaiface.h)
description: The IBDA_ IPV4Filter interface is implemented on a Network Provider.
helpviewer_keywords: ["IBDA_IPV4Filter","IBDA_IPV4Filter interface [Microsoft TV Technologies]","IBDA_IPV4Filter interface [Microsoft TV Technologies]","described","IBDA_IPV4FilterInterface","bdaiface/IBDA_IPV4Filter","mstv.ibda_ipv4filter"]
old-location: mstv\ibda_ipv4filter.htm
tech.root: mstv
ms.assetid: 3db86e21-6d05-4b7f-be83-a3fa506a0e3b
ms.date: 12/05/2018
ms.keywords: IBDA_IPV4Filter, IBDA_IPV4Filter interface [Microsoft TV Technologies], IBDA_IPV4Filter interface [Microsoft TV Technologies],described, IBDA_IPV4FilterInterface, bdaiface/IBDA_IPV4Filter, mstv.ibda_ipv4filter
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
 - IBDA_IPV4Filter
 - bdaiface/IBDA_IPV4Filter
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
 - IBDA_IPV4Filter
---

# IBDA_IPV4Filter interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

The <b>IBDA_ IPV4Filter</b> interface is implemented on a Network Provider. The methods are called by the BDA IPSink filter in order to give the Network Provider a list of multicast Ethernet addresses being requested by an application. The Network Provider then informs all registered transport information filters (TIFs) of the new addresses. The TIF(s) are responsible for mapping those addresses to PIDs and passing the PIDs back to the Network Provider, which then resets the PID list for the IP data output pin on the MPEG-2 Demultiplexer. This causes the IP data on the specified PIDs to be routed through the data services segment of the graph and on to Winsock where the listening application can receive it. The <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ethernetfilter">IBDA_EthernetFilter</a> interface performs the same function for Ethernet multicast addresses.

## -inheritance

The <b>IBDA_IPV4Filter</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_IPV4Filter</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_ IPV4Filter)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
