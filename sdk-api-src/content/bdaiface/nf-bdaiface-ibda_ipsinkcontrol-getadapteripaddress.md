---
UID: NF:bdaiface.IBDA_IPSinkControl.GetAdapterIPAddress
title: IBDA_IPSinkControl::GetAdapterIPAddress (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["GetAdapterIPAddress","GetAdapterIPAddress method [Microsoft TV Technologies]","GetAdapterIPAddress method [Microsoft TV Technologies]","IBDA_IPSinkControl interface","IBDA_IPSinkControl interface [Microsoft TV Technologies]","GetAdapterIPAddress method","IBDA_IPSinkControl.GetAdapterIPAddress","IBDA_IPSinkControl::GetAdapterIPAddress","IBDA_IPSinkControlGetAdapterIPAddress","bdaiface/IBDA_IPSinkControl::GetAdapterIPAddress","mstv.ibda_ipsinkcontrol_getadapteripaddress"]
old-location: mstv\ibda_ipsinkcontrol_getadapteripaddress.htm
tech.root: mstv
ms.assetid: ce9710e6-f611-4457-a282-9a7677b3055e
ms.date: 12/05/2018
ms.keywords: GetAdapterIPAddress, GetAdapterIPAddress method [Microsoft TV Technologies], GetAdapterIPAddress method [Microsoft TV Technologies],IBDA_IPSinkControl interface, IBDA_IPSinkControl interface [Microsoft TV Technologies],GetAdapterIPAddress method, IBDA_IPSinkControl.GetAdapterIPAddress, IBDA_IPSinkControl::GetAdapterIPAddress, IBDA_IPSinkControlGetAdapterIPAddress, bdaiface/IBDA_IPSinkControl::GetAdapterIPAddress, mstv.ibda_ipsinkcontrol_getadapteripaddress
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
 - IBDA_IPSinkControl::GetAdapterIPAddress
 - bdaiface/IBDA_IPSinkControl::GetAdapterIPAddress
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
 - IBDA_IPSinkControl.GetAdapterIPAddress
---

# IBDA_IPSinkControl::GetAdapterIPAddress


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>GetAdapterIPAddress</b> method retrieves the IP address of the NIC.

## -parameters

### -param pulcbSize [out]

Receives the length of the buffer, in bytes.

### -param pbBuffer [out]

Pointer to a byte array containing the address.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

<b>IBDA_IPSinkControl</b> is no longer being supported for Ring 3 clients. Use the <b>BDA_IPSinkInfo</b> interface instead.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkcontrol">IBDA_IPSinkControl Interface</a>