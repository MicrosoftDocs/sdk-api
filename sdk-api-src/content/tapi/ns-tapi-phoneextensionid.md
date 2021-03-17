---
UID: NS:tapi.phoneextensionid_tag
title: PHONEEXTENSIONID (tapi.h)
description: The PHONEEXTENSIONID structure describes an extension identifier.
helpviewer_keywords: ["*LPPHONEEXTENSIONID","LPPHONEEXTENSIONID","LPPHONEEXTENSIONID structure pointer [TAPI 2.2]","PHONEEXTENSIONID","PHONEEXTENSIONID structure [TAPI 2.2]","_tapi2_phoneextensionid_str","tapi/LPPHONEEXTENSIONID","tapi/PHONEEXTENSIONID","tapi2.phoneextensionid_str"]
old-location: tapi2\phoneextensionid_str.htm
tech.root: tapi3
ms.assetid: 61f376fd-2287-4425-9445-163f71aebf04
ms.date: 12/05/2018
ms.keywords: '*LPPHONEEXTENSIONID, LPPHONEEXTENSIONID, LPPHONEEXTENSIONID structure pointer [TAPI 2.2], PHONEEXTENSIONID, PHONEEXTENSIONID structure [TAPI 2.2], _tapi2_phoneextensionid_str, tapi/LPPHONEEXTENSIONID, tapi/PHONEEXTENSIONID, tapi2.phoneextensionid_str'
req.header: tapi.h
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
req.typenames: PHONEEXTENSIONID, *LPPHONEEXTENSIONID
req.redist: 
ms.custom: 19H1
f1_keywords:
 - phoneextensionid_tag
 - tapi/phoneextensionid_tag
 - LPPHONEEXTENSIONID
 - tapi/LPPHONEEXTENSIONID
 - PHONEEXTENSIONID
 - tapi/PHONEEXTENSIONID
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tapi.h
api_name:
 - PHONEEXTENSIONID
---

# PHONEEXTENSIONID structure


## -description

The 
<b>PHONEEXTENSIONID</b> structure describes an extension identifier. Extension identifiers are used to identify service provider-specific extensions for phone device classes. The 
<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a> and 
<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetextensionid">TSPI_phoneGetExtensionID</a> functions return this structure.

## -struct-fields

### -field dwExtensionID0

First part of the extension identifier.

### -field dwExtensionID1

Second part of the extension identifier.

### -field dwExtensionID2

Third part of the extension identifier.

### -field dwExtensionID3

Fourth part of the extension identifier.

## -remarks

These four members together specify a universally unique extension identifier that identifies a phone device class extension. This structure may not be extended.

Extension identifiers are generated using an SDK-provided generation utility.

## -see-also

<a href="/windows/desktop/api/tspi/nf-tspi-tspi_phonegetextensionid">TSPI_phoneGetExtensionID</a>



<a href="/windows/desktop/api/tapi/nf-tapi-phonenegotiateapiversion">phoneNegotiateAPIVersion</a>