---
UID: NN:tapi3.ITMSPAddress
title: ITMSPAddress (tapi3.h)
description: The ITMSPAddress interface (tapi3.h) is implemented by the MSP and represents a media service provider to the TAPI DLL.
helpviewer_keywords: ["ITMSPAddress","ITMSPAddress interface [TAPI 2.2]","ITMSPAddress interface [TAPI 2.2]","described","_tapi3_itmspaddress","msp/ITMSPAddress","tapi3.itmspaddress"]
old-location: tapi3\itmspaddress.htm
tech.root: tapi3
ms.assetid: 246a0bcd-0dbb-4b77-a1cd-e6378eaff889
ms.date: 08/09/2022
ms.keywords: ITMSPAddress, ITMSPAddress interface [TAPI 2.2], ITMSPAddress interface [TAPI 2.2],described, _tapi3_itmspaddress, msp/ITMSPAddress, tapi3.itmspaddress
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
 - ITMSPAddress
 - tapi3/ITMSPAddress
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
 - ITMSPAddress
---

# ITMSPAddress interface


## -description

The 
<b>ITMSPAddress</b> interface is implemented by the MSP and represents a media service provider to the TAPI DLL. It is not exposed to end-user or server applications. TAPI 3 will call <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cocreateinstance">CoCreateInstance</a> on this interface to create the MSP object.

## -inheritance

The <b>ITMSPAddress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITMSPAddress</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstreamcontrol">ITStreamControl</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstream">ITSubStream</a>



<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itsubstreamcontrol">ITSubStreamControl</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
