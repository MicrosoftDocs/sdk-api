---
UID: NF:tapi3.ITMSPAddress.Initialize
title: ITMSPAddress::Initialize (tapi3.h)
description: The ITMSPAddress::Initialize (tapi3.h) method is called when the MSP is loaded.
helpviewer_keywords: ["ITMSPAddress interface [TAPI 2.2]","Initialize method","ITMSPAddress.Initialize","ITMSPAddress::Initialize","Initialize","Initialize method [TAPI 2.2]","Initialize method [TAPI 2.2]","ITMSPAddress interface","_tapi3_itmspaddress_initialize","msp/ITMSPAddress::Initialize","tapi3.itmspaddress_initialize"]
old-location: tapi3\itmspaddress_initialize.htm
tech.root: tapi3
ms.assetid: 5df2c486-0133-4705-8d37-10b56b40c85d
ms.date: 08/09/2022
ms.keywords: ITMSPAddress interface [TAPI 2.2],Initialize method, ITMSPAddress.Initialize, ITMSPAddress::Initialize, Initialize, Initialize method [TAPI 2.2], Initialize method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_initialize, msp/ITMSPAddress::Initialize, tapi3.itmspaddress_initialize
req.header: tapi3.h
req.include-header: Tapi3.h
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
 - ITMSPAddress::Initialize
 - tapi3/ITMSPAddress::Initialize
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - msp.h
api_name:
 - ITMSPAddress.Initialize
---

# ITMSPAddress::Initialize


## -description

The 
<b>Initialize</b> method is called when the MSP is loaded.

## -parameters

### -param hEvent [in]

TAPI 3's handle for this MSP.

## -returns

This method can return one of these values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_OUTOFMEMORY</b></dt>
</dl>
</td>
<td width="60%">
Insufficient memory exists to perform operation.

</td>
</tr>
</table>

## -remarks

If an MSP is written using the MSP base classes, this method initializes data members, creates the Terminal Manager, and calls Start on the global MSP thread object.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itmspaddress">ITMSPAddress</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
