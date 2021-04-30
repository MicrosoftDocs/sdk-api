---
UID: NF:bdaiface.IBDA_IPSinkInfo.get_AdapterIPAddress
title: IBDA_IPSinkInfo::get_AdapterIPAddress (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["IBDA_IPSinkInfo interface [Microsoft TV Technologies]","get_AdapterIPAddress method","IBDA_IPSinkInfo.get_AdapterIPAddress","IBDA_IPSinkInfo::get_AdapterIPAddress","IBDA_IPSinkInfoget_AdapterIPAddress","bdaiface/IBDA_IPSinkInfo::get_AdapterIPAddress","get_AdapterIPAddress","get_AdapterIPAddress method [Microsoft TV Technologies]","get_AdapterIPAddress method [Microsoft TV Technologies]","IBDA_IPSinkInfo interface","mstv.ibda_ipsinkinfo_get_adapteripaddress"]
old-location: mstv\ibda_ipsinkinfo_get_adapteripaddress.htm
tech.root: mstv
ms.assetid: 3518bad7-d732-4ef7-a8b6-135193eaf9d6
ms.date: 12/05/2018
ms.keywords: IBDA_IPSinkInfo interface [Microsoft TV Technologies],get_AdapterIPAddress method, IBDA_IPSinkInfo.get_AdapterIPAddress, IBDA_IPSinkInfo::get_AdapterIPAddress, IBDA_IPSinkInfoget_AdapterIPAddress, bdaiface/IBDA_IPSinkInfo::get_AdapterIPAddress, get_AdapterIPAddress, get_AdapterIPAddress method [Microsoft TV Technologies], get_AdapterIPAddress method [Microsoft TV Technologies],IBDA_IPSinkInfo interface, mstv.ibda_ipsinkinfo_get_adapteripaddress
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
 - IBDA_IPSinkInfo::get_AdapterIPAddress
 - bdaiface/IBDA_IPSinkInfo::get_AdapterIPAddress
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
 - IBDA_IPSinkInfo.get_AdapterIPAddress
---

# IBDA_IPSinkInfo::get_AdapterIPAddress


## -description

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_AdapterIPAddress</b> method retrieves the IP address of the data that the IP Sink filter receives. This address is assigned by the system; it is not guaranteed to be the same for any two instances of the IP Sink filter.

## -parameters

### -param pbstrBuffer [out]

Pointer to a <b>BSTR</b> that receives the IP address. The returned string has the form <code>N.N.N.N</code>; for example, <code>3.0.0.0</code>.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The caller must free the returned string, using the <b>SysFreeString</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkinfo">IBDA_IPSinkInfo Interface</a>