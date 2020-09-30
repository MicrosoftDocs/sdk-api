---
UID: NS:wincrypt._CERT_OTHER_LOGOTYPE_INFO
title: CERT_OTHER_LOGOTYPE_INFO (wincrypt.h)
description: Contains information about logo types that are not predefined.
helpviewer_keywords: ["*PCERT_OTHER_LOGOTYPE_INFO","CERT_OTHER_LOGOTYPE_INFO","CERT_OTHER_LOGOTYPE_INFO structure [Security]","PCERT_OTHER_LOGOTYPE_INFO","PCERT_OTHER_LOGOTYPE_INFO structure pointer [Security]","security.cert_other_logotype_info","szOID_BACKGROUND_OTHER_LOGOTYPE","szOID_LOYALTY_OTHER_LOGOTYPE","wincrypt/CERT_OTHER_LOGOTYPE_INFO","wincrypt/PCERT_OTHER_LOGOTYPE_INFO"]
old-location: security\cert_other_logotype_info.htm
tech.root: security
ms.assetid: 104cc412-a268-4b5f-bb9d-9df27f4df6b7
ms.date: 12/05/2018
ms.keywords: '*PCERT_OTHER_LOGOTYPE_INFO, CERT_OTHER_LOGOTYPE_INFO, CERT_OTHER_LOGOTYPE_INFO structure [Security], PCERT_OTHER_LOGOTYPE_INFO, PCERT_OTHER_LOGOTYPE_INFO structure pointer [Security], security.cert_other_logotype_info, szOID_BACKGROUND_OTHER_LOGOTYPE, szOID_LOYALTY_OTHER_LOGOTYPE, wincrypt/CERT_OTHER_LOGOTYPE_INFO, wincrypt/PCERT_OTHER_LOGOTYPE_INFO'
req.header: wincrypt.h
req.include-header: 
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
req.typenames: CERT_OTHER_LOGOTYPE_INFO, *PCERT_OTHER_LOGOTYPE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_OTHER_LOGOTYPE_INFO
 - wincrypt/_CERT_OTHER_LOGOTYPE_INFO
 - PCERT_OTHER_LOGOTYPE_INFO
 - wincrypt/PCERT_OTHER_LOGOTYPE_INFO
 - CERT_OTHER_LOGOTYPE_INFO
 - wincrypt/CERT_OTHER_LOGOTYPE_INFO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_OTHER_LOGOTYPE_INFO
---

# CERT_OTHER_LOGOTYPE_INFO structure


## -description

The <b>CERT_OTHER_LOGOTYPE_INFO</b> structure contains information about logo types that are not predefined.

## -struct-fields

### -field pszObjId

The address of a null-terminated ANSI string that contains the object identifier of the logo type. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="szOID_LOYALTY_OTHER_LOGOTYPE"></a><a id="szoid_loyalty_other_logotype"></a><a id="SZOID_LOYALTY_OTHER_LOGOTYPE"></a><dl>
<dt><b>szOID_LOYALTY_OTHER_LOGOTYPE</b></dt>
<dt>"1.3.6.1.5.5.7.20.1"</dt>
</dl>
</td>
<td width="60%">
The logo is a loyalty logo.

</td>
</tr>
<tr>
<td width="40%"><a id="szOID_BACKGROUND_OTHER_LOGOTYPE"></a><a id="szoid_background_other_logotype"></a><a id="SZOID_BACKGROUND_OTHER_LOGOTYPE"></a><dl>
<dt><b>szOID_BACKGROUND_OTHER_LOGOTYPE</b></dt>
<dt>"1.3.6.1.5.5.7.20.2"</dt>
</dl>
</td>
<td width="60%">
The logo is a background logo.

</td>
</tr>
</table>

### -field LogotypeInfo

A <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_info">CERT_LOGOTYPE_INFO</a> structure that contains the logo type information.