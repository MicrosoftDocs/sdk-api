---
UID: NE:tsgpolicyengine.__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0001
title: "__MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0001"
author: windows-sdk-content
description: Specifies the type of authentication used to connect to Remote Desktop Gateway (RD Gateway).
old-location: termserv\aaauthschemes.htm
old-project: TermServ
ms.assetid: ff80f8ac-8378-4087-aa95-a081d2dd710a
ms.author: windowssdkdev
ms.date: 07/09/2018
ms.keywords: AAAuthSchemes, AAAuthSchemes enumeration [Remote Desktop Services], AA_AUTH_ANY, AA_AUTH_BASIC, AA_AUTH_CONID, AA_AUTH_COOKIE, AA_AUTH_DIGEST, AA_AUTH_LOGGEDONCREDENTIALS, AA_AUTH_MAX, AA_AUTH_MIN, AA_AUTH_NEGOTIATE, AA_AUTH_NTLM, AA_AUTH_ORGID, AA_AUTH_SC, __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0001, termserv.aaauthschemes, tsgpolicyengine/AAAuthSchemes, tsgpolicyengine/AA_AUTH_ANY, tsgpolicyengine/AA_AUTH_BASIC, tsgpolicyengine/AA_AUTH_CONID, tsgpolicyengine/AA_AUTH_COOKIE, tsgpolicyengine/AA_AUTH_DIGEST, tsgpolicyengine/AA_AUTH_LOGGEDONCREDENTIALS, tsgpolicyengine/AA_AUTH_MAX, tsgpolicyengine/AA_AUTH_MIN, tsgpolicyengine/AA_AUTH_NEGOTIATE, tsgpolicyengine/AA_AUTH_NTLM, tsgpolicyengine/AA_AUTH_ORGID, tsgpolicyengine/AA_AUTH_SC
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: tsgpolicyengine.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7
req.target-min-winversvr: Windows Server 2008 R2
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: TSGPolicyEngine.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: AAAuthSchemes
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Tsgpolicyengine.h
 - TSGPolicyEngine.h
api_name:
 - AAAuthSchemes
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# __MIDL___MIDL_itf_tsgpolicyengine_0000_0000_0001 enumeration


## -description


Specifies the type of authentication used to connect to Remote Desktop Gateway (RD Gateway).


## -enum-fields




### -field AA_AUTH_MIN

This value is reserved.


### -field AA_AUTH_BASIC

Basic protocol authentication.


### -field AA_AUTH_NTLM

NTLM protocol authentication.


### -field AA_AUTH_SC

Standard authentication.


### -field AA_AUTH_LOGGEDONCREDENTIALS

Windows logon credentials authentication.


### -field AA_AUTH_NEGOTIATE

Microsoft Negotiate authentication.


### -field AA_AUTH_ANY

This value is reserved.


### -field AA_AUTH_COOKIE

Cookie-based authentication.


### -field AA_AUTH_DIGEST

Digest access authentication.


### -field AA_AUTH_ORGID

Claims-based authentication.

<b>Windows Server 2012, Windows 8, Windows Server 2008 R2 and Windows 7:  </b>Not supported.


### -field AA_AUTH_CONID

Authentication by reverse connection ID.

<b>Windows Server 2012 R2, Windows 8.1, Windows Server 2012, Windows 8, Windows Server 2008 R2 and Windows 7:  </b>Not supported.


### -field AA_AUTH_SSPI_NTLM


### -field AA_AUTH_MAX

This value is reserved.


## -see-also




<a href="https://msdn.microsoft.com/1c79f910-8dd9-47dc-80d1-f6252f0a43dd">AAAccountingData</a>
 

 

