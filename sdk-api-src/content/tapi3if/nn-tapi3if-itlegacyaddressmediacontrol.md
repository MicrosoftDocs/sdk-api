---
UID: NN:tapi3if.ITLegacyAddressMediaControl
title: ITLegacyAddressMediaControl (tapi3if.h)
description: The ITLegacyAddressMediaControl interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the Address Object and can be created by calling QueryInterface on ITAddress.
helpviewer_keywords: ["ITLegacyAddressMediaControl","ITLegacyAddressMediaControl interface [TAPI 2.2]","ITLegacyAddressMediaControl interface [TAPI 2.2]","described","_tapi3_itlegacyaddressmediacontrol","tapi3.itlegacyaddressmediacontrol","tapi3if/ITLegacyAddressMediaControl"]
old-location: tapi3\itlegacyaddressmediacontrol.htm
tech.root: tapi3
ms.assetid: 5f3d0189-fc9d-4fa5-bc8e-a0abf1f607f8
ms.date: 12/05/2018
ms.keywords: ITLegacyAddressMediaControl, ITLegacyAddressMediaControl interface [TAPI 2.2], ITLegacyAddressMediaControl interface [TAPI 2.2],described, _tapi3_itlegacyaddressmediacontrol, tapi3.itlegacyaddressmediacontrol, tapi3if/ITLegacyAddressMediaControl
req.header: tapi3if.h
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
req.lib: Uuid.lib
req.dll: Tapi3.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITLegacyAddressMediaControl
 - tapi3if/ITLegacyAddressMediaControl
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Tapi3.dll
api_name:
 - ITLegacyAddressMediaControl
---

# ITLegacyAddressMediaControl interface


## -description

The 
<b>ITLegacyAddressMediaControl</b> interface is provided to support legacy applications that require direct access to a device and its configuration. It is exposed by the 
<a href="/windows/desktop/Tapi/address-object">Address Object</a> and can be created by calling <b>QueryInterface</b> on 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>.

The 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2">ITLegacyAddressMediaControl2</a> interface derives from the 
<b>ITLegacyAddressMediaControl</b> interface. 
<b>ITLegacyAddressMediaControl2</b> provides additional methods that allow the configuration of parameters related to line devices.

## -inheritance

The <b>ITLegacyAddressMediaControl</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ITLegacyAddressMediaControl</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itlegacyaddressmediacontrol2">ITLegacyAddressMediaControl2</a>
