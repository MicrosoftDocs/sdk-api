---
UID: NF:ntsecpkg.CredMarshalTargetInfo
title: CredMarshalTargetInfo function
author: windows-driver-content
description: Serializes the specified target into an array of byte values.
old-location: security\credmarshaltargetinfo.htm
old-project: SecAuthN
ms.assetid: 1e50a135-e8b3-4aa6-a3b0-f4b1490310e5
ms.author: windowsdriverdev
ms.date: 5/7/2018
ms.keywords: CredMarshalTargetInfo, CredMarshalTargetInfo function [Security], ntsecpkg/CredMarshalTargetInfo, security.credmarshaltargetinfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntsecpkg.h
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
req.typenames: SECPKG_SESSIONINFO_TYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	CredMarshalTargetInfo
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# CredMarshalTargetInfo function


## -description


Serializes the specified target into an array of byte values.


## -parameters




### -param InTargetInfo [in]

A pointer to a <a href="https://msdn.microsoft.com/264f6cb6-36c6-4cdb-b7bb-a5dbd332adcb">Unicode</a> version of the <a href="https://msdn.microsoft.com/92180f2c-ef7c-4481-9b6f-19234c114afb">CREDENTIAL_TARGET_INFORMATION</a> structure that specifies the target to serialize.


### -param Buffer [out]

The serialized array of byte values that represents the target specified by the <i>InTargetInfo</i> parameter.


### -param BufferSize

The size, in bytes, of the <i>Buffer</i> array.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code that indicates the reason it failed.



