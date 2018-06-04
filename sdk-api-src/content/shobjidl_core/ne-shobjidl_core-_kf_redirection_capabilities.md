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

# _KF_REDIRECTION_CAPABILITIES enumeration


## -description


Flags that specify the current redirection capabilities of a known folder. Used by <a href="https://msdn.microsoft.com/5abc4944-1fd7-400a-817d-b58a7f4989ea">IKnownFolder::GetRedirectionCapabilities</a>.


## -enum-fields




### -field KF_REDIRECTION_CAPABILITIES_ALLOW_ALL

The folder can be redirected if any of the bits in the lower byte of the value are set but no DENY flag is set. DENY flags are found in the upper byte of the value.


### -field KF_REDIRECTION_CAPABILITIES_REDIRECTABLE

The folder can be redirected. Currently, redirection exists for only common and user folders; fixed and virtual folders cannot be redirected.


### -field KF_REDIRECTION_CAPABILITIES_DENY_ALL

Redirection is not allowed.


### -field KF_REDIRECTION_CAPABILITIES_DENY_POLICY_REDIRECTED

The folder cannot be redirected because it is already redirected by group policy.


### -field KF_REDIRECTION_CAPABILITIES_DENY_POLICY

The folder cannot be redirected because the policy prohibits redirecting this folder.


### -field KF_REDIRECTION_CAPABILITIES_DENY_PERMISSIONS

The folder cannot be redirected because the calling application does not have sufficient permissions.


## -see-also




<a href="https://msdn.microsoft.com/49799A9E-BA86-4977-B5F3-590BE1E5FBF6">Known Folders Sample</a>
 

 

