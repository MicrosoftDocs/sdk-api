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

# _SECPKG_EXTENDED_INFORMATION_CLASS enumeration


## -description



			The <b>SECPKG_EXTENDED_INFORMATION_CLASS</b> enumeration describes the type of information to set or get for a <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security package</a>.

This enumeration is used by the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> and 
<a href="https://msdn.microsoft.com/a6176786-c19b-4ecf-8a7b-2430ff8b56f7">SpSetExtendedInformation</a> functions.


## -enum-fields




### -field SecpkgGssInfo

GSS OID information used to identify the security package in GSS-compatible negotiations.


### -field SecpkgContextThunks

Identifies the calls to the 
<a href="https://msdn.microsoft.com/67bc087f-7519-4c8a-9b34-b3ecd306a334">QueryContextAttributes (General)</a> function that are handled in the <a href="https://msdn.microsoft.com/65dd9a04-fc7c-4179-95ff-dac7dad4668f">Local Security Authority</a> (LSA) process space (LSA mode) rather than being handled in the client process space (user mode).


### -field SecpkgMutualAuthLevel

The mutual authentication level used in the system. This value is valid for the 
<a href="https://msdn.microsoft.com/e3cb602a-2c98-4e9c-bfbc-f12f353ce3e3">SpGetExtendedInformation</a> function only.


### -field SecpkgWowClientDll

Identifies that the WOW client supports a 32-bit version. Otherwise, the WOW client expects the process to run in 64-bit mode. LSA operations are done by the 64-bit version. When the security context is handed back to the client,  the 32-bit WOW-aware version is loaded and hands it any information from the 64-bit version.


### -field SecpkgExtraOids

Identifies that extra object identifiers (OIDs) are available.


### -field SecpkgMaxInfo

The end value for the enumeration. This value is not a valid parameter value.


### -field SecpkgNego2Info

Identifies the SPNego information for the security package.

<b>Windows Server 2008, Windows Vista, Windows Server 2003 and Windows XP:  </b>This constant is not available.

