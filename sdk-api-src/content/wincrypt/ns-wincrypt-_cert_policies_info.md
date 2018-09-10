---
UID: NS:wincrypt._CERT_POLICIES_INFO
title: "_CERT_POLICIES_INFO"
author: windows-sdk-content
description: The CERT_POLICIES_INFO structure contains an array of CERT_POLICY_INFO.
old-location: security\cert_policies_info.htm
tech.root: seccrypto
ms.assetid: cf5fafd9-6129-4f25-8d61-189b46585e57
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: "*PCERT_POLICIES_INFO, CERT_POLICIES_INFO, CERT_POLICIES_INFO structure [Security], PCERT_POLICIES_INFO, PCERT_POLICIES_INFO structure pointer [Security], _CERT_POLICIES_INFO, _crypto2_cert_policies_info, security.cert_policies_info, wincrypt/CERT_POLICIES_INFO, wincrypt/PCERT_POLICIES_INFO"
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_POLICIES_INFO
product: Windows
targetos: Windows
req.typenames: CERT_POLICIES_INFO, *PCERT_POLICIES_INFO
req.redist: 
---

# _CERT_POLICIES_INFO structure


## -description


The <b>CERT_POLICIES_INFO</b> structure contains an array of 
<a href="https://msdn.microsoft.com/0d6396fe-99f6-4f66-9f01-55582d24ddc1">CERT_POLICY_INFO</a>.


<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a> creates an instance of this structure when performed on a 
<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a> structure's <b>Value</b> member with the structure's <b>pszObjId</b> member set to szOID_CERT_POLICIES.

An instance of this structure can be used as input to 
<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a> to create an appropriate <a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>.


## -struct-fields




### -field cPolicyInfo

Number of elements in the <b>rgPolicyInfo</b> array.
					


### -field rgPolicyInfo

Array of 
<a href="https://msdn.microsoft.com/0d6396fe-99f6-4f66-9f01-55582d24ddc1">CERT_POLICY_INFO</a> structures.


## -see-also




<a href="https://msdn.microsoft.com/787a4df0-c0e3-46b9-a7e6-eb3bee3ed717">CERT_EXTENSION</a>



<a href="https://msdn.microsoft.com/0d6396fe-99f6-4f66-9f01-55582d24ddc1">CERT_POLICY_INFO</a>



<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>
 

 

