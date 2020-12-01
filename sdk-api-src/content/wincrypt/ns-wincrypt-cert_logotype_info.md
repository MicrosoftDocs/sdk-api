---
UID: NS:wincrypt._CERT_LOGOTYPE_INFO
title: CERT_LOGOTYPE_INFO (wincrypt.h)
description: Contains information about logotype data.
helpviewer_keywords: ["*PCERT_LOGOTYPE_INFO","CERT_LOGOTYPE_DIRECT_INFO_CHOICE","CERT_LOGOTYPE_INDIRECT_INFO_CHOICE","CERT_LOGOTYPE_INFO","CERT_LOGOTYPE_INFO structure [Security]","PCERT_LOGOTYPE_INFO","PCERT_LOGOTYPE_INFO structure pointer [Security]","security.cert_logotype_info","wincrypt/CERT_LOGOTYPE_INFO","wincrypt/PCERT_LOGOTYPE_INFO"]
old-location: security\cert_logotype_info.htm
tech.root: security
ms.assetid: 7ce801bf-38fd-4490-8465-40ed5078bbff
ms.date: 12/05/2018
ms.keywords: '*PCERT_LOGOTYPE_INFO, CERT_LOGOTYPE_DIRECT_INFO_CHOICE, CERT_LOGOTYPE_INDIRECT_INFO_CHOICE, CERT_LOGOTYPE_INFO, CERT_LOGOTYPE_INFO structure [Security], PCERT_LOGOTYPE_INFO, PCERT_LOGOTYPE_INFO structure pointer [Security], security.cert_logotype_info, wincrypt/CERT_LOGOTYPE_INFO, wincrypt/PCERT_LOGOTYPE_INFO'
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
req.typenames: CERT_LOGOTYPE_INFO, *PCERT_LOGOTYPE_INFO
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _CERT_LOGOTYPE_INFO
 - wincrypt/_CERT_LOGOTYPE_INFO
 - PCERT_LOGOTYPE_INFO
 - wincrypt/PCERT_LOGOTYPE_INFO
 - CERT_LOGOTYPE_INFO
 - wincrypt/CERT_LOGOTYPE_INFO
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
 - CERT_LOGOTYPE_INFO
---

# CERT_LOGOTYPE_INFO structure


## -description

The <b>CERT_LOGOTYPE_INFO</b> structure contains information about logotype data.

## -struct-fields

### -field dwLogotypeInfoChoice

Specifies the type of logotype data. This can be one of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_DIRECT_INFO_CHOICE"></a><a id="cert_logotype_direct_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_DIRECT_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The logotype data is available directly. The <b>pLogotypeDirectInfo</b> member contains the actual logotype data.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_LOGOTYPE_INDIRECT_INFO_CHOICE"></a><a id="cert_logotype_indirect_info_choice"></a><dl>
<dt><b>CERT_LOGOTYPE_INDIRECT_INFO_CHOICE</b></dt>
</dl>
</td>
<td width="60%">
The logotype data is available through a reference. The <b>pLogotypeIndirectInfo</b> member contains a reference to the logotype information.

</td>
</tr>
</table>

### -field DUMMYUNIONNAME

### -field DUMMYUNIONNAME.pLogotypeDirectInfo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_data">CERT_LOGOTYPE_DATA</a> structure that contains the actual logotype data. This member is only used if the <b>dwLogotypeInfoChoice</b> member contains <b>CERT_LOGOTYPE_DIRECT_INFO_CHOICE</b>.

### -field DUMMYUNIONNAME.pLogotypeIndirectInfo

The address of a <a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_reference">CERT_LOGOTYPE_REFERENCE</a> structure that contains references to the logotype data. This member is only used if the <b>dwLogotypeInfoChoice</b> member contains <b>CERT_LOGOTYPE_INDIRECT_INFO_CHOICE</b>.

## -see-also

<a href="/windows/desktop/api/wincrypt/ns-wincrypt-cert_logotype_ext_info">CERT_LOGOTYPE_EXT_INFO</a>