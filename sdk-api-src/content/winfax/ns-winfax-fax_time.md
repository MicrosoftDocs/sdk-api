---
UID: NS:winfax._FAX_TIME
title: FAX_TIME (winfax.h)
description: The FAX_TIME structure represents a time, using individual members for the current hour and minute. The time is expressed in Coordinated Universal Time (UTC).
helpviewer_keywords: ["*PFAX_TIME","FAX_TIME","FAX_TIME structure [Fax Service]","FAX_TIMEA","FAX_TIMEW","PFAX_TIME","PFAX_TIME structure pointer [Fax Service]","_mfax_fax_time_str","fax._mfax_fax_time_str","winfax/FAX_TIME","winfax/FAX_TIMEA","winfax/FAX_TIMEW","winfax/PFAX_TIME"]
old-location: fax\_mfax_fax_time_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_24fm.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_TIME, FAX_TIME, FAX_TIME structure [Fax Service], FAX_TIMEA, FAX_TIMEW, PFAX_TIME, PFAX_TIME structure pointer [Fax Service], _mfax_fax_time_str, fax._mfax_fax_time_str, winfax/FAX_TIME, winfax/FAX_TIMEA, winfax/FAX_TIMEW, winfax/PFAX_TIME'
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_TIMEW (Unicode) and FAX_TIMEA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: FAX_TIME, *PFAX_TIME
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_TIME
 - winfax/_FAX_TIME
 - PFAX_TIME
 - winfax/PFAX_TIME
 - FAX_TIME
 - winfax/FAX_TIME
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Winfax.h
api_name:
 - FAX_TIME
 - FAX_TIMEA
 - FAX_TIMEW
---

# FAX_TIME structure


## -description

The <b>FAX_TIME</b> structure represents a time, using individual members for the current hour and minute. The time is expressed in Coordinated Universal Time (UTC).

## -struct-fields

### -field Hour

Type: <b>WORD</b>

Specifies a 16-bit unsigned integer that is the current hour. Valid values are 0 through 23.

### -field Minute

Type: <b>WORD</b>

Specifies a 16-bit unsigned integer that is the current minute. Valid values are 0 through 59.

## -remarks

The <a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a> structure includes a <b>FAX_TIME</b> structure to describe the discount period that applies when a fax server is sending fax transmissions.

## -see-also

<a href="/windows/desktop/api/winfax/ns-winfax-fax_configurationa">FAX_CONFIGURATION</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxgetconfigurationa">FaxGetConfiguration</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetconfigurationa">FaxSetConfiguration</a>