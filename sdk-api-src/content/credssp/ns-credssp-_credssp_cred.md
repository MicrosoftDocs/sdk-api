---
UID: NS:credssp._CREDSSP_CRED
title: "_CREDSSP_CRED"
author: windows-sdk-content
description: Specifies authentication data for both Schannel and Negotiate security packages.
old-location: security\credssp_cred.htm
tech.root: secauthn
ms.assetid: b22bd22c-e6e1-4817-b5cf-ab49f574e75f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*PCREDSSP_CRED, CREDSSP_CRED, CREDSSP_CRED structure [Security], PCREDSSP_CRED, PCREDSSP_CRED structure pointer [Security], _CREDSSP_CRED, credssp/CREDSSP_CRED, credssp/PCREDSSP_CRED, security.credssp_cred"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: credssp.h
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
 - Credssp.h
api_name:
 - CREDSSP_CRED
product: Windows
targetos: Windows
req.typenames: CREDSSP_CRED, *PCREDSSP_CRED
req.redist: 
---

# _CREDSSP_CRED structure


## -description


 The <b>CREDSSP_CRED</b> structure specifies authentication data for both Schannel and Negotiate <a href="https://msdn.microsoft.com/en-us/library/ms721625(v=VS.85).aspx">security packages</a>.


## -struct-fields




### -field Type

The <a href="https://msdn.microsoft.com/en-us/library/Aa965488(v=VS.85).aspx">CREDSPP_SUBMIT_TYPE</a> enumeration value that specifies the type of credentials contained in this structure.


### -field pSchannelCred

A pointer to a set of Schannel credentials.


### -field pSpnegoCred

A pointer to a set of Negotiate credentials.


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965463(v=VS.85).aspx">AcquireCredentialsHandle (CredSSP)</a>



<a href="https://msdn.microsoft.com/en-us/library/Aa965488(v=VS.85).aspx">CREDSPP_SUBMIT_TYPE</a>
 

 

