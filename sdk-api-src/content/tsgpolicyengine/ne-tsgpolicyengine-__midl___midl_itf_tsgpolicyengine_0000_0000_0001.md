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
 

 

