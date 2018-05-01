---
UID: NF:ntlsa.LsaQueryCAPs
title: LsaQueryCAPs function
author: windows-driver-content
description: Returns the Central Access Policies (CAPs) for the specified IDs.
old-location: security\lsaquerycaps.htm
old-project: SecAuthN
ms.assetid: 55D6FD6F-0FD5-41F6-967B-F5600E19C3EF
ms.author: windowsdriverdev
ms.date: 4/24/2018
ms.keywords: LsaQueryCAPs, LsaQueryCAPs function [Security], ntlsa/LsaQueryCAPs, security.lsaquerycaps
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ntlsa.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: VBS_ENCLAVE_REPORT_VARDATA_HEADER
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Advapi32.dll
api_name:
-	LsaQueryCAPs
product: Windows
targetos: Windows
req.lib: Advapi32.lib
req.dll: Advapi32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# LsaQueryCAPs function


## -description


Returns the Central Access Policies (CAPs) for the specified IDs.


## -parameters




### -param CAPIDs

A pointer to a variable that contains an array of pointers to CAPIDs that identify the CAPs being queried.


### -param CAPIDCount [in]

The number of IDs in the <i>CAPIDs</i> parameter.


### -param CAPs [out]

Receives a pointer to an array of pointers to <a href="https://msdn.microsoft.com/C1C2E8AE-0B7F-4620-9C27-31DAF683E342">CENTRAL_ACCESS_POLICY</a> structures representing the queried CAPs.


### -param CAPCount [out]

The number of <a href="https://msdn.microsoft.com/C1C2E8AE-0B7F-4620-9C27-31DAF683E342">CENTRAL_ACCESS_POLICY</a> structure pointers returned in the <i>CAPs</i> parameter.


## -returns



If the function succeeds, the return value is STATUS_SUCCESS.

If the function fails, the return value is an NTSTATUS code, which can be one of the <a href="https://msdn.microsoft.com/ee55364e-8ffe-4a78-a49a-250756561770">LSA Policy Function Return Values</a>.



