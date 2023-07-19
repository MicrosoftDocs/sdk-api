---
UID: NF:bdaiface.IBDA_IPSinkInfo.get_MulticastList
title: IBDA_IPSinkInfo::get_MulticastList (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["IBDA_IPSinkInfo interface [Microsoft TV Technologies]","get_MulticastList method","IBDA_IPSinkInfo.get_MulticastList","IBDA_IPSinkInfo::get_MulticastList","IBDA_IPSinkInfoget_MulticastList","bdaiface/IBDA_IPSinkInfo::get_MulticastList","get_MulticastList","get_MulticastList method [Microsoft TV Technologies]","get_MulticastList method [Microsoft TV Technologies]","IBDA_IPSinkInfo interface","mstv.ibda_ipsinkinfo_get_multicastlist"]
old-location: mstv\ibda_ipsinkinfo_get_multicastlist.htm
tech.root: mstv
ms.assetid: 29375c69-5e45-4fc5-98d2-1cc1c750b809
ms.date: 12/05/2018
ms.keywords: IBDA_IPSinkInfo interface [Microsoft TV Technologies],get_MulticastList method, IBDA_IPSinkInfo.get_MulticastList, IBDA_IPSinkInfo::get_MulticastList, IBDA_IPSinkInfoget_MulticastList, bdaiface/IBDA_IPSinkInfo::get_MulticastList, get_MulticastList, get_MulticastList method [Microsoft TV Technologies], get_MulticastList method [Microsoft TV Technologies],IBDA_IPSinkInfo interface, mstv.ibda_ipsinkinfo_get_multicastlist
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
 - IBDA_IPSinkInfo::get_MulticastList
 - bdaiface/IBDA_IPSinkInfo::get_MulticastList
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
 - IBDA_IPSinkInfo.get_MulticastList
---

# IBDA_IPSinkInfo::get_MulticastList


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_MulticastList</b> method retrieves a list of the multicast addresses to which the IP Sink filter is listening. This method returns a list of IP addresses in 6-byte IEEE 802.3 format; the list is returned as an array of bytes.

## -parameters

### -param pulcbAddresses [out]

Receives the number of bytes in the returned array.

### -param ppbAddressList [out]

Pointer to variable that receives an array of bytes, of size *<i>pulcbAddresses</i>. Each IP address is 6 consecutive bytes.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The method allocates the memory for the array. The caller must free the memory by calling <b>CoTaskMemFree</b>.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkinfo">IBDA_IPSinkInfo Interface</a>