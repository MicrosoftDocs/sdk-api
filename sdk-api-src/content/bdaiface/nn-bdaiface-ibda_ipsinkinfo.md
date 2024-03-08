---
UID: NN:bdaiface.IBDA_IPSinkInfo
title: IBDA_IPSinkInfo (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems.
helpviewer_keywords: ["IBDA_IPSinkInfo","IBDA_IPSinkInfo interface [Microsoft TV Technologies]","IBDA_IPSinkInfo interface [Microsoft TV Technologies]","described","IBDA_IPSinkInfoInterface","bdaiface/IBDA_IPSinkInfo","mstv.ibda_ipsinkinfo"]
old-location: mstv\ibda_ipsinkinfo.htm
tech.root: mstv
ms.assetid: fbbe12ea-964a-4a83-ac0a-ac8808bd9a63
ms.date: 12/05/2018
ms.keywords: IBDA_IPSinkInfo, IBDA_IPSinkInfo interface [Microsoft TV Technologies], IBDA_IPSinkInfo interface [Microsoft TV Technologies],described, IBDA_IPSinkInfoInterface, bdaiface/IBDA_IPSinkInfo, mstv.ibda_ipsinkinfo
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
 - IBDA_IPSinkInfo
 - bdaiface/IBDA_IPSinkInfo
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
 - IBDA_IPSinkInfo
---

# IBDA_IPSinkInfo interface


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        

The <b>IBDA_IPSinkInfo</b> interface is implemented on the <a href="/previous-versions/windows/desktop/mstv/bda-ip-sink-filter">BDA IP Sink</a> filter, which manages the delivery of in-band IP data to the network stack. This interface supersedes <a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkcontrol">IBDA_IPSinkControl</a>.

## -inheritance

The <b>IBDA_IPSinkInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IBDA_IPSinkInfo</b> also has these types of members:
<ul>
<li><a href="/">Methods</a></li>
</ul>

## -remarks

To declare the interface identifier (IID) for this interface, use the <b>__uuidof</b> operator: <code>__uuidof(IBDA_IPSinkInfo)</code>.

## -see-also

<a href="/previous-versions/windows/desktop/mstv/bda-interfaces">BDA Interfaces</a>
