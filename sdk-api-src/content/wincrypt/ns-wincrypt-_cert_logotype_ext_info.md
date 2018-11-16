---
UID: NS:wincrypt._CERT_LOGOTYPE_EXT_INFO
title: "_CERT_LOGOTYPE_EXT_INFO"
author: windows-sdk-content
description: Contains a set of logotype information.
old-location: security\cert_logotype_ext_info.htm
tech.root: SecCrypto
ms.assetid: 5013241b-439e-4aea-9161-699ee69c65c9
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PCERT_LOGOTYPE_EXT_INFO, CERT_LOGOTYPE_EXT_INFO, CERT_LOGOTYPE_EXT_INFO structure [Security], PCERT_LOGOTYPE_EXT_INFO, PCERT_LOGOTYPE_EXT_INFO structure pointer [Security], _CERT_LOGOTYPE_EXT_INFO, security.cert_logotype_ext_info, wincrypt/CERT_LOGOTYPE_EXT_INFO, wincrypt/PCERT_LOGOTYPE_EXT_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Wincrypt.h
api_name:
 - CERT_LOGOTYPE_EXT_INFO
product: Windows
targetos: Windows
req.typenames: CERT_LOGOTYPE_EXT_INFO, *PCERT_LOGOTYPE_EXT_INFO
req.redist: 
---

# _CERT_LOGOTYPE_EXT_INFO structure


## -description


The <b>CERT_LOGOTYPE_EXT_INFO</b> structure contains a set of logotype information.


## -struct-fields




### -field cCommunityLogo

The number of elements in the <b>rgCommunityLogo</b> array.


### -field rgCommunityLogo

An array of <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structures that contain the community logotypes. The <b>cCommunityLogo</b>  member contains the number of elements in this array.


### -field pIssuerLogo

The address of a <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structure that contains the issuer logotype. This member is optional and may be <b>NULL</b>.


### -field pSubjectLogo

The address of a <a href="https://msdn.microsoft.com/7ce801bf-38fd-4490-8465-40ed5078bbff">CERT_LOGOTYPE_INFO</a> structure that contains the subject logotype. This member is optional and may be <b>NULL</b>.


### -field cOtherLogo

The number of elements in the <b>rgOtherLogo</b> array.


### -field rgOtherLogo

An array of <a href="https://msdn.microsoft.com/104cc412-a268-4b5f-bb9d-9df27f4df6b7">CERT_OTHER_LOGOTYPE_INFO</a> structures that contain any other logotypes. The <b>cOtherLogo</b>  member contains the number of elements in this array.


## -see-also




<a href="https://msdn.microsoft.com/7d5ed4f4-9d76-4a16-9059-27b0edd83459">CryptDecodeObject</a>



<a href="https://msdn.microsoft.com/9576a2a7-4379-4c1b-8ad5-284720cf7ccc">CryptEncodeObject</a>



<a href="https://msdn.microsoft.com/45134db8-059b-43d3-90c2-9b6cc970fca0">CryptEncodeObjectEx</a>
 

 

