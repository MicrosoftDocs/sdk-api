---
UID: NS:wincrypt._CERT_BASIC_CONSTRAINTS2_INFO
title: "_CERT_BASIC_CONSTRAINTS2_INFO"
author: windows-sdk-content
description: The CERT_BASIC_CONSTRAINTS2_INFO structure contains information indicating whether the certified subject can act as a CA or an end entity. If the subject can act as a CA, a certification path length constraint can also be specified.
old-location: security\cert_basic_constraints2_info.htm
old-project: seccrypto
ms.assetid: bbeeb18b-c5d7-4490-8edc-4af19b37ab3f
ms.author: windowssdkdev
ms.date: 06/05/2018
ms.keywords: "*PCERT_BASIC_CONSTRAINTS2_INFO, CERT_BASIC_CONSTRAINTS2_INFO, CERT_BASIC_CONSTRAINTS2_INFO structure [Security], PCERT_BASIC_CONSTRAINTS2_INFO, PCERT_BASIC_CONSTRAINTS2_INFO structure pointer [Security], _CERT_BASIC_CONSTRAINTS2_INFO, _crypto2_cert_basic_constraints2_info, security.cert_basic_constraints2_info, wincrypt/CERT_BASIC_CONSTRAINTS2_INFO, wincrypt/PCERT_BASIC_CONSTRAINTS2_INFO"
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: wincrypt.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CERT_BASIC_CONSTRAINTS2_INFO, *PCERT_BASIC_CONSTRAINTS2_INFO
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_BASIC_CONSTRAINTS2_INFO
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _CERT_BASIC_CONSTRAINTS2_INFO structure


## -description


The <b>CERT_BASIC_CONSTRAINTS2_INFO</b> structure contains information indicating whether the certified subject can act as a CA or an end entity. If the subject can act as a CA, a certification path length constraint can also be specified.


<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with the structure's <b>pszObjId</b> member set to szOID_BASIC_CONSTRAINTS2.

An instance of this structure can be used as input to <a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.


## -struct-fields




### -field fCA

Boolean indicating whether the certificate subject can act as a <a href="https://msdn.microsoft.com/db46def4-bfdc-4801-a57d-d568e94a2dbb">certification authority</a> (CA) or not.


### -field fPathLenConstraint

Boolean indicating whether the <b>dwPathLenConstraint</b> field limits the maximum length of the certification path. Used only if <b>fCA</b> is <b>TRUE</b>.


### -field dwPathLenConstraint

Maximum number of CA certificates that can follow this certificate in a certification path. A value of zero indicates that the subject of this certificate can issue certificates only to end entities and not to other CAs. Used only if both <b>fCA</b> and <b>fPathLenConstraint</b> are <b>TRUE</b>.

