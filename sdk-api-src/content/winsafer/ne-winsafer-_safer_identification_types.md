---
UID: NE:winsafer._SAFER_IDENTIFICATION_TYPES
title: "_SAFER_IDENTIFICATION_TYPES"
author: windows-sdk-content
description: Defines the possible types of identification rule structures that can be identified by the SAFER_IDENTIFICATION_HEADER structure.
old-location: security\safer_identification_types.htm
old-project: SecMgmt
ms.assetid: ced40d58-e9f1-47cc-9e05-fdaa253bb16b
ms.author: windowssdkdev
ms.date: 05/25/2018
ms.keywords: SAFER_IDENTIFICATION_TYPES, SAFER_IDENTIFICATION_TYPES enumeration [Security], SaferIdentityDefault, SaferIdentityTypeCertificate, SaferIdentityTypeImageHash, SaferIdentityTypeImageName, SaferIdentityTypeUrlZone, _SAFER_IDENTIFICATION_TYPES, security.safer_identification_types, winsafer/SAFER_IDENTIFICATION_TYPES, winsafer/SaferIdentityDefault, winsafer/SaferIdentityTypeCertificate, winsafer/SaferIdentityTypeImageHash, winsafer/SaferIdentityTypeImageName, winsafer/SaferIdentityTypeUrlZone
ms.prod: windows
ms.technology: windows-sdk
ms.topic: enum
req.header: winsafer.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: VALENTW (Unicode) and VALENTA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SAFER_IDENTIFICATION_TYPES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	WinSafer.h
api_name:
-	SAFER_IDENTIFICATION_TYPES
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# _SAFER_IDENTIFICATION_TYPES enumeration


## -description


The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type defines the possible types of identification rule structures that can be identified by the  <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure.


## -enum-fields




### -field SaferIdentityDefault

The header is for a default level structure.


### -field SaferIdentityTypeImageName

The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeImageHash

The header is for a <a href="https://msdn.microsoft.com/68b4b5f5-8220-4180-8243-b6f1fd7826bd">SAFER_HASH_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeUrlZone

The header is for a <a href="https://msdn.microsoft.com/8f165956-9ef0-469e-a71b-f9341a347e59">SAFER_URLZONE_IDENTIFICATION</a> structure.


### -field SaferIdentityTypeCertificate

The header is for a <a href="https://msdn.microsoft.com/d845a750-2931-4c17-be78-92843e2bd76f">SAFER_PATHNAME_IDENTIFICATION</a> structure.


## -remarks



The <b>SAFER_IDENTIFICATION_TYPES</b> enumeration type is used by the <a href="https://msdn.microsoft.com/9bcb7d22-2360-4146-9972-118ba8822aa7">SAFER_IDENTIFICATION_HEADER</a> structure.



