---
UID: NS:ksopmapi._OPM_OMAC
title: OPM_OMAC (ksopmapi.h)
description: The OPM_OMAC (ksopmapi.h) structure contains a Message Authentication Code (MAC) for an Output Protection Manager (OPM) message.
helpviewer_keywords: ["OPM_OMAC","OPM_OMAC structure [Media Foundation]","_OPM_OMAC","ksopmapi/OPM_OMAC","mf.opm_omac"]
old-location: mf\opm_omac.htm
tech.root: mf
ms.assetid: 6ff37a2a-9e63-4097-8ee6-bcc4bd580ab8
ms.date: 08/05/2022
ms.keywords: OPM_OMAC, OPM_OMAC structure [Media Foundation], _OPM_OMAC, ksopmapi/OPM_OMAC, mf.opm_omac
req.header: ksopmapi.h
req.include-header: Opmapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: OPM_OMAC
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _OPM_OMAC
 - ksopmapi/_OPM_OMAC
 - OPM_OMAC
 - ksopmapi/OPM_OMAC
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - ksopmapi.h
api_name:
 - OPM_OMAC
---

# OPM_OMAC structure


## -description

Contains a Message Authentication Code (MAC) for an <a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a> (OPM) message.

## -struct-fields

### -field abOMAC

A buffer that contains the cryptographic MAC value of the message.

## -see-also

<a href="/windows/desktop/medfound/opm-structures">OPM Structures</a>



<a href="/windows/desktop/api/opmapi/ns-opmapi-opm_configure_parameters">OPM_CONFIGURE_PARAMETERS</a>



<a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_get_info_parameters">OPM_GET_INFO_PARAMETERS</a>



<a href="/windows/desktop/api/ksopmapi/ns-ksopmapi-opm_requested_information">OPM_REQUESTED_INFORMATION</a>



<a href="/windows/desktop/medfound/output-protection-manager">Output Protection Manager</a>
