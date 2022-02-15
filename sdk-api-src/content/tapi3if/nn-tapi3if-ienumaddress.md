---
UID: NN:tapi3if.IEnumAddress
title: IEnumAddress (tapi3if.h)
description: The IEnumAddress interface provides COM-standard enumeration methods for the ITAddress interface. The ITTAPI::EnumerateAddresses and ITAgentHandler::EnumerateUsableAddresses methods return a pointer to IEnumAddress.
helpviewer_keywords: ["IEnumAddress","IEnumAddress interface [TAPI 2.2]","IEnumAddress interface [TAPI 2.2]","described","_tapi3_ienumaddress","tapi3.ienumaddress","tapi3if/IEnumAddress"]
old-location: tapi3\ienumaddress.htm
tech.root: tapi3
ms.assetid: bfe9f12e-ceb7-4120-8193-70feb2bc7c85
ms.date: 12/05/2018
ms.keywords: IEnumAddress, IEnumAddress interface [TAPI 2.2], IEnumAddress interface [TAPI 2.2],described, _tapi3_ienumaddress, tapi3.ienumaddress, tapi3if/IEnumAddress
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
 - IEnumAddress
 - tapi3if/IEnumAddress
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
 - IEnumAddress
---

# IEnumAddress interface


## -description

The 
<b>IEnumAddress</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a> interface. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-ittapi-enumerateaddresses">ITTAPI::EnumerateAddresses</a> and 
<a href="/windows/desktop/api/tapi3/nf-tapi3-itagenthandler-enumerateusableaddresses">ITAgentHandler::EnumerateUsableAddresses</a> methods return a pointer to 
<b>IEnumAddress</b>.

The 
<b>IEnumAddress</b> interface is hidden from Visual Basic and scripting languages.

## -inheritance

The <b>IEnumAddress</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumAddress</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itaddress">ITAddress</a>
