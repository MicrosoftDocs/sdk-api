---
UID: NF:bdaiface.IBDA_IPSinkInfo.get_AdapterDescription
title: IBDA_IPSinkInfo::get_AdapterDescription (bdaiface.h)
description: This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
helpviewer_keywords: ["IBDA_IPSinkInfo interface [Microsoft TV Technologies]","get_AdapterDescription method","IBDA_IPSinkInfo.get_AdapterDescription","IBDA_IPSinkInfo::get_AdapterDescription","IBDA_IPSinkInfoget_AdapterDescription","bdaiface/IBDA_IPSinkInfo::get_AdapterDescription","get_AdapterDescription","get_AdapterDescription method [Microsoft TV Technologies]","get_AdapterDescription method [Microsoft TV Technologies]","IBDA_IPSinkInfo interface","mstv.ibda_ipsinkinfo_get_adapterdescription"]
old-location: mstv\ibda_ipsinkinfo_get_adapterdescription.htm
tech.root: mstv
ms.assetid: 68b41304-2043-4cbf-8872-7f3d9f3b7a83
ms.date: 12/05/2018
ms.keywords: IBDA_IPSinkInfo interface [Microsoft TV Technologies],get_AdapterDescription method, IBDA_IPSinkInfo.get_AdapterDescription, IBDA_IPSinkInfo::get_AdapterDescription, IBDA_IPSinkInfoget_AdapterDescription, bdaiface/IBDA_IPSinkInfo::get_AdapterDescription, get_AdapterDescription, get_AdapterDescription method [Microsoft TV Technologies], get_AdapterDescription method [Microsoft TV Technologies],IBDA_IPSinkInfo interface, mstv.ibda_ipsinkinfo_get_adapterdescription
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
 - IBDA_IPSinkInfo::get_AdapterDescription
 - bdaiface/IBDA_IPSinkInfo::get_AdapterDescription
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
 - IBDA_IPSinkInfo.get_AdapterDescription
---

# IBDA_IPSinkInfo::get_AdapterDescription


## -description

\[The feature associated with this page, [Microsoft TV Technologies](/previous-versions/windows/desktop/mstv/microsoft-tv-technologies-portal), is a legacy feature. Microsoft strongly recommends that new code does not use this feature.\]

This interface is available for use in the Microsoft Windows 2000, Windows XP, and Windows Server 2003 operating systems. It may be altered or unavailable in subsequent versions.
        



The <b>get_AdapterDescription</b> method retrieves the description of the network adapter.

## -parameters

### -param pbstrBuffer [out]

Pointer to a <b>BSTR</b> that receives the description.

## -returns

If the method succeeds, it returns S_OK. If it fails, it returns an error code.

## -remarks

The caller must free the returned string, using the <b>SysFreeString</b> method.

## -see-also

<a href="/windows/desktop/DirectShow/error-and-success-codes">Error and Success Codes</a>



<a href="/windows/desktop/api/bdaiface/nn-bdaiface-ibda_ipsinkinfo">IBDA_IPSinkInfo Interface</a>