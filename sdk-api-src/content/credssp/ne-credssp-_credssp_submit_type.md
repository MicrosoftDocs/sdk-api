---
UID: NE:credssp._CREDSSP_SUBMIT_TYPE
title: "_CREDSSP_SUBMIT_TYPE"
author: windows-sdk-content
description: Specifies the type of credentials specified by a CREDSSP_CRED structure.
old-location: security\credspp_submit_type.htm
old-project: secauthn
ms.assetid: d30e219b-ea39-41da-b714-3ceb13a5614d
ms.author: windowssdkdev
ms.date: 08/20/2018
ms.keywords: CREDSPP_SUBMIT_TYPE, CREDSPP_SUBMIT_TYPE enumeration [Security], CredsspCertificateCreds, CredsspPasswordCreds, CredsspSchannelCreds, CredsspSubmitBufferBoth, CredsspSubmitBufferBothOld, _CREDSSP_SUBMIT_TYPE, credssp/CREDSPP_SUBMIT_TYPE, credssp/CredsspCertificateCreds, credssp/CredsspPasswordCreds, credssp/CredsspSchannelCreds, credssp/CredsspSubmitBufferBoth, credssp/CredsspSubmitBufferBothOld, security.credspp_submit_type
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: credssp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Credentialprovider.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: CREDSPP_SUBMIT_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Credssp.h
api_name:
 - CREDSPP_SUBMIT_TYPE
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
---

# _CREDSSP_SUBMIT_TYPE enumeration


## -description


The <b>CREDSPP_SUBMIT_TYPE</b> enumeration specifies the type of credentials specified by a <a href="https://msdn.microsoft.com/en-us/library/Aa965581(v=VS.85).aspx">CREDSSP_CRED</a> structure.


## -enum-fields




### -field CredsspPasswordCreds

The credentials are a user name and password.


### -field CredsspSchannelCreds

The credentials are Schannel credentials.


### -field CredsspCertificateCreds

The credentials are in a certificate.


### -field CredsspSubmitBufferBoth

The credentials contain both certificate and Schannel credentials.


### -field CredsspSubmitBufferBothOld


### -field CredsspCredEx




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Aa965581(v=VS.85).aspx">CREDSSP_CRED</a>
 

 

