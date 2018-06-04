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

# _LSA_TOKEN_INFORMATION_TYPE enumeration


## -description


The <b>LSA_TOKEN_INFORMATION_TYPE</b> enumeration specifies the levels of information that can be included in a logon token.

When the LSA calls either 
<a href="https://msdn.microsoft.com/4c8def77-d536-486e-a830-9df3848fbccb">LsaApLogonUser</a>, 
<a href="https://msdn.microsoft.com/7778292a-7062-4f49-b4a9-6784e5e4ccd7">LsaApLogonUserEx</a>, or 
<a href="https://msdn.microsoft.com/002ac773-bd46-49b5-b54c-6b8f5d5ef9f7">LsaApLogonUserEx2</a> the <a href="https://msdn.microsoft.com/0baaa937-f635-4500-8dcd-9dbbd6f4cd02">authentication package</a> is expected to return one of the following enumeration values to indicate the type of token information structure returned.


## -enum-fields




### -field LsaTokenInformationNull

The token information is stored in an 
<a href="https://msdn.microsoft.com/fbcd0f78-1ad5-4bea-a95f-d19fb3894537">LSA_TOKEN_INFORMATION_NULL</a> structure. 




This token information type is used for anonymous logons or <b>null</b> sessions, where a token is needed but the client's identity is unknown.

For example, a non-authenticated network circuit (such as a domain controller's <b>null</b> session) can be given <b>NULL</b> information. In this case, an anonymous token is generated for the logon. An anonymous token does not permit access to protected system resources, but does allow access to unprotected system resources.


### -field LsaTokenInformationV1

The token information is stored in a 
<a href="https://msdn.microsoft.com/e4c43828-aa5c-443c-93ad-96bb986533c5">LSA_TOKEN_INFORMATION_V1</a> structure. This structure contains information that an authentication package can place in a Version 1 Windows token object. A Version 1 Windows token object stores all the information needed to build a token and is used in most logon cases. The LSA creates the token object, and returns a handle to that token object to the caller of 
<a href="https://msdn.microsoft.com/75968d53-5af2-4d77-9486-26403b73c954">LsaLogonUser</a>.


### -field LsaTokenInformationV2


### -field LsaTokenInformationV3



