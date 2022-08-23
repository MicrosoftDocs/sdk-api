---
UID: NF:msp.ITMSPAddress.Shutdown
title: ITMSPAddress::Shutdown (msp.h)
description: The ITMSPAddress::Shutdown (msp.h) method is called when the MSP is unloaded. Shutdown will be called once per address object.
helpviewer_keywords: ["ITMSPAddress interface [TAPI 2.2]","Shutdown method","ITMSPAddress.Shutdown","ITMSPAddress::Shutdown","Shutdown","Shutdown method [TAPI 2.2]","Shutdown method [TAPI 2.2]","ITMSPAddress interface","_tapi3_itmspaddress_shutdown","msp/ITMSPAddress::Shutdown","tapi3.itmspaddress_shutdown"]
old-location: tapi3\itmspaddress_shutdown.htm
tech.root: tapi3
ms.assetid: 877691cb-b12b-4389-b93c-4ff13a52f4d7
ms.date: 08/08/2022
ms.keywords: ITMSPAddress interface [TAPI 2.2],Shutdown method, ITMSPAddress.Shutdown, ITMSPAddress::Shutdown, Shutdown, Shutdown method [TAPI 2.2], Shutdown method [TAPI 2.2],ITMSPAddress interface, _tapi3_itmspaddress_shutdown, msp/ITMSPAddress::Shutdown, tapi3.itmspaddress_shutdown
req.header: msp.h
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
 - ITMSPAddress::Shutdown
 - msp/ITMSPAddress::Shutdown
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
 - ITMSPAddress.Shutdown
---

# ITMSPAddress::Shutdown


## -description

The 
<b>Shutdown</b> method is called when the MSP is unloaded. 
<b>Shutdown</b> will be called once per address object.



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
<dt><b>E_NOTIMPL</b></dt>
</dl>
</td>
<td width="60%">
Method not implemented.

</td>
</tr>
</table>

## -remarks

This method releases the terminals and releases the Terminal Manager. It releases all unprocessed events, and calls 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itmediacontrol-stop">Stop</a> on the global MSP thread object. When this function is called, no call should be alive. However, bugs in the application may keep calls or terminals around.

## -see-also

<a href="/windows/desktop/api/msp/nn-msp-itmspaddress">ITMSPAddress</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
