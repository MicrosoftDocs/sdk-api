---
UID: NS:lpmapi.ERROR_SPEC
title: ERROR_SPEC (lpmapi.h)
description: The ERROR_SPEC structure contains RSVP error messages.
helpviewer_keywords: ["ERROR_SPEC","ERROR_SPEC structure [QOS]","lpmapi/ERROR_SPEC","qos.error_spec"]
old-location: qos\error_spec.htm
tech.root: QOS
ms.assetid: 4d20cbb8-c29a-4c0c-bf06-532144da3e33
ms.date: 12/05/2018
ms.keywords: ERROR_SPEC, ERROR_SPEC structure [QOS], lpmapi/ERROR_SPEC, qos.error_spec
req.header: lpmapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: ERROR_SPEC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ERROR_SPEC
 - lpmapi/ERROR_SPEC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lpmapi.h
api_name:
 - ERROR_SPEC
---

# ERROR_SPEC structure


## -description

The 
<b>ERROR_SPEC</b> structure contains RSVP error messages.

## -struct-fields

### -field errs_header

Error header, in the form of an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a> structure.

### -field errs_u

Union containing RSVP error information.



#### errs_ipv4

Error information, expressed as an <a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-error_spec_ipv4">Error_Spec_IPv4</a> structure.

### -field errs_ipv4

## -see-also

<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-error_spec_ipv4">Error_Spec_IPv4</a>



<a href="/previous-versions/windows/desktop/api/lpmapi/ns-lpmapi-rsvpobjhdr">RsvpObjHdr</a>

