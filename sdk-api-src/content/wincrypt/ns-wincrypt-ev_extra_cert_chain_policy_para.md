---
UID: NS:wincrypt._EV_EXTRA_CERT_CHAIN_POLICY_PARA
title: EV_EXTRA_CERT_CHAIN_POLICY_PARA (wincrypt.h)
description: Specifies the parameters that are passed in for EV policy validation. Applications use this structure to pass hints to the API that indicate which of the policy qualifier flags of the extended validation certificates are important to the application.
helpviewer_keywords: ["*PEV_EXTRA_CERT_CHAIN_POLICY_PARA","CERT_ROOT_PROGRAM_FLAG_LSC","CERT_ROOT_PROGRAM_FLAG_ORG","CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO","EV_EXTRA_CERT_CHAIN_POLICY_PARA","EV_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security]","PEV_EXTRA_CERT_CHAIN_POLICY_PARA","PEV_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security]","security.ev_extra_cert_chain_policy_para","wincrypt/EV_EXTRA_CERT_CHAIN_POLICY_PARA","wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_PARA"]
old-location: security\ev_extra_cert_chain_policy_para.htm
tech.root: security
ms.assetid: 64ea96a7-ba37-49e1-a73f-ce772c1a9fb2
ms.date: 12/05/2018
ms.keywords: '*PEV_EXTRA_CERT_CHAIN_POLICY_PARA, CERT_ROOT_PROGRAM_FLAG_LSC, CERT_ROOT_PROGRAM_FLAG_ORG, CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO, EV_EXTRA_CERT_CHAIN_POLICY_PARA, EV_EXTRA_CERT_CHAIN_POLICY_PARA structure [Security], PEV_EXTRA_CERT_CHAIN_POLICY_PARA, PEV_EXTRA_CERT_CHAIN_POLICY_PARA structure pointer [Security], security.ev_extra_cert_chain_policy_para, wincrypt/EV_EXTRA_CERT_CHAIN_POLICY_PARA, wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_PARA'
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.typenames: EV_EXTRA_CERT_CHAIN_POLICY_PARA, *PEV_EXTRA_CERT_CHAIN_POLICY_PARA
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _EV_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/_EV_EXTRA_CERT_CHAIN_POLICY_PARA
 - PEV_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/PEV_EXTRA_CERT_CHAIN_POLICY_PARA
 - EV_EXTRA_CERT_CHAIN_POLICY_PARA
 - wincrypt/EV_EXTRA_CERT_CHAIN_POLICY_PARA
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
 - EV_EXTRA_CERT_CHAIN_POLICY_PARA
---

# EV_EXTRA_CERT_CHAIN_POLICY_PARA structure


## -description

The <b>EV_EXTRA_CERT_CHAIN_POLICY_PARA</b> structure specifies the parameters that are  passed in for EV policy validation. Applications use this structure to pass hints to the API that indicate which of the  policy qualifier flags of the extended validation certificates are important to the application.

## -struct-fields

### -field cbSize

The size, in bytes, of this structure.

### -field dwRootProgramQualifierFlags

A <b>DWORD</b> value that specifies which of the EV policy qualifier bits are required for validation. The value of this parameter can be a Bitwise combination of zero or more of the following values.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_LSC"></a><a id="cert_root_program_flag_lsc"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_LSC</b></dt>
<dt>0x40</dt>
</dl>
</td>
<td width="60%">
Validation of the Locale (L), State (S), and Country (C) fields in
the subject name meets Root Program Requirements for display.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_ORG"></a><a id="cert_root_program_flag_org"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_ORG</b></dt>
<dt>0x80</dt>
</dl>
</td>
<td width="60%">
Validation of the Organization (O) field in the subject name meets Root Program Requirements for display.

</td>
</tr>
<tr>
<td width="40%"><a id="CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO"></a><a id="cert_root_program_flag_subject_logo"></a><dl>
<dt><b>CERT_ROOT_PROGRAM_FLAG_SUBJECT_LOGO</b></dt>
<dt>0x20</dt>
</dl>
</td>
<td width="60%">
Validation of the  Subject logotype meets Root Program Requirements for display.

</td>
</tr>
</table>

