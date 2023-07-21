---
UID: NF:bdaiface.IBDA_IPSinkControl.GetMulticastList
title: IBDA_IPSinkControl::GetMulticastList (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["GetMulticastList","GetMulticastList method [Microsoft TV Technologies]","GetMulticastList method [Microsoft TV Technologies]","IBDA_IPSinkControl interface","IBDA_IPSinkControl interface [Microsoft TV Technologies]","GetMulticastList method","IBDA_IPSinkControl.GetMulticastList","IBDA_IPSinkControl::GetMulticastList","IBDA_IPSinkControlGetMulticastList","bdaiface/IBDA_IPSinkControl::GetMulticastList","mstv.ibda_ipsinkcontrol_getmulticastlist"]
old-location: mstv\ibda_ipsinkcontrol_getmulticastlist.htm
tech.root: mstv
ms.assetid: 005cce5c-e8fb-49f0-8a75-b05cdd1f5e1b
ms.date: 12/05/2018
ms.keywords: GetMulticastList, GetMulticastList method [Microsoft TV Technologies], GetMulticastList method [Microsoft TV Technologies],IBDA_IPSinkControl interface, IBDA_IPSinkControl interface [Microsoft TV Technologies],GetMulticastList method, IBDA_IPSinkControl.GetMulticastList, IBDA_IPSinkControl::GetMulticastList, IBDA_IPSinkControlGetMulticastList, bdaiface/IBDA_IPSinkControl::GetMulticastList, mstv.ibda_ipsinkcontrol_getmulticastlist
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
 - IBDA_IPSinkControl::GetMulticastList
 - bdaiface/IBDA_IPSinkControl::GetMulticastList
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
 - IBDA_IPSinkControl.GetMulticastList
---

# IBDA_IPSinkControl::GetMulticastList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>GetMulticastList</b> method retrieves a list of the multicast addresses to which the IP Sink filter is listening.

## -parameters

### -param pulcbSize [out]

Receives the length of the buffer, in bytes.

### -param pbBuffer [out]

Pointer to a byte array containing the multicast list.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<b>IBDA_IPSinkControl</b> is no longer being supported for Ring 3 clients. Use the <b>BDA_IPSinkInfo</b> interface instead.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkcontrol">IBDA_IPSinkControl Interface</a>