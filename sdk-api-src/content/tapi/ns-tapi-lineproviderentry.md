---
UID: NS:tapi.lineproviderentry_tag
title: LINEPROVIDERENTRY (tapi.h)
description: The LINEPROVIDERENTRY structure provides the information for a single service provider entry. An array of these structures is returned as part of the LINEPROVIDERLIST structure returned by the function lineGetProviderList.
helpviewer_keywords: ["*LPLINEPROVIDERENTRY","LINEPROVIDERENTRY","LINEPROVIDERENTRY structure [TAPI 2.2]","LPLINEPROVIDERENTRY","LPLINEPROVIDERENTRY structure pointer [TAPI 2.2]","_tapi2_lineproviderentry_str","tapi/LINEPROVIDERENTRY","tapi/LPLINEPROVIDERENTRY","tapi2.lineproviderentry_str"]
old-location: tapi2\lineproviderentry_str.htm
tech.root: tapi3
ms.assetid: e54a8244-e773-441f-a387-b3b22c4a0a54
ms.date: 12/05/2018
ms.keywords: '*LPLINEPROVIDERENTRY, LINEPROVIDERENTRY, LINEPROVIDERENTRY structure [TAPI 2.2], LPLINEPROVIDERENTRY, LPLINEPROVIDERENTRY structure pointer [TAPI 2.2], _tapi2_lineproviderentry_str, tapi/LINEPROVIDERENTRY, tapi/LPLINEPROVIDERENTRY, tapi2.lineproviderentry_str'
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
req.typenames: LINEPROVIDERENTRY, *LPLINEPROVIDERENTRY
req.redist: 
ms.custom: 19H1
f1_keywords:
 - lineproviderentry_tag
 - tapi/lineproviderentry_tag
 - LPLINEPROVIDERENTRY
 - tapi/LPLINEPROVIDERENTRY
 - LINEPROVIDERENTRY
 - tapi/LINEPROVIDERENTRY
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
 - LINEPROVIDERENTRY
---

# LINEPROVIDERENTRY structure


## -description

The 
<b>LINEPROVIDERENTRY</b> structure provides the information for a single service provider entry. An array of these structures is returned as part of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderlist">LINEPROVIDERLIST</a> structure returned by the function 
<a href="/windows/desktop/api/tapi/nf-tapi-linegetproviderlist">lineGetProviderList</a>.

## -struct-fields

### -field dwPermanentProviderID

Permanent provider identifier of the entry.

### -field dwProviderFilenameSize

Size of the provider file name string, including the <b>null</b> terminator, in bytes.

### -field dwProviderFilenameOffset

Offset from the beginning of the 
<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderlist">LINEPROVIDERLIST</a> structure to a <b>null</b>-terminated string containing the file name (path) of the service provider DLL (.TSP) file. The size of the string is specified by <b>dwProviderFilenameSize</b>.

## -remarks

Not extensible.

## -see-also

<a href="/windows/desktop/api/tapi/ns-tapi-lineproviderlist">LINEPROVIDERLIST</a>



<a href="/windows/desktop/api/tapi/nf-tapi-linegetproviderlist">lineGetProviderList</a>