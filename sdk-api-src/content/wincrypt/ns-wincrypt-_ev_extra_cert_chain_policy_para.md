---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# _EV_EXTRA_CERT_CHAIN_POLICY_PARA structure


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
 

