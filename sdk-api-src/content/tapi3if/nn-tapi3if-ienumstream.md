---
UID: NN:tapi3if.IEnumStream
title: IEnumStream (tapi3if.h)
description: The IEnumStream interface provides COM-standard enumeration methods for the ITStream interface. The ITStreamControl::EnumerateStreams and ITParticipant::EnumerateStreams methods return a pointer to IEnumStream.
helpviewer_keywords: ["IEnumStream","IEnumStream interface [TAPI 2.2]","IEnumStream interface [TAPI 2.2]","described","_tapi3_ienumstream","tapi3.ienumstream","tapi3if/IEnumStream"]
old-location: tapi3\ienumstream.htm
tech.root: tapi3
ms.assetid: 52e8c040-8bc5-4c9c-a697-ec05164adea2
ms.date: 12/05/2018
ms.keywords: IEnumStream, IEnumStream interface [TAPI 2.2], IEnumStream interface [TAPI 2.2],described, _tapi3_ienumstream, tapi3.ienumstream, tapi3if/IEnumStream
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IEnumStream
 - tapi3if/IEnumStream
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - tapi3if.h
api_name:
 - IEnumStream
---

# IEnumStream interface


## -description

The 
<b>IEnumStream</b> interface provides COM-standard enumeration methods for the 
<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a> interface. The 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">ITStreamControl::EnumerateStreams</a> and 
<a href="/windows/desktop/api/tapi3if/nf-tapi3if-itstreamcontrol-enumeratestreams">ITParticipant::EnumerateStreams</a> methods return a pointer to 
<b>IEnumStream</b>.

## -inheritance

The <b>IEnumStream</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumStream</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/tapi3if/nn-tapi3if-itstream">ITStream</a>



<a href="/windows/desktop/Tapi/media-service-provider-interface-mspi-">Media Service Provider Interface (MSPI)</a>
