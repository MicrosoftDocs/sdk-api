---
UID: NF:ual.UalStart
title: UalStart function
author: windows-driver-content
description: Starts a User Access Logging (UAL) session.
old-location: ual\ualstart.htm
old-project: ual
ms.assetid: 800E8BCF-39A1-490A-9B6A-12EE900B8D17
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: UalStart, UalStart function [User Access Logging], ual.ualstart, ual/UalStart
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: ual.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: RECORD_READING_POLICY
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Ualapi.dll
api_name:
-	UalStart
product: Windows
targetos: Windows
req.lib: Ualapi.lib
req.dll: Ualapi.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UalStart function


## -description


Starts a User Access Logging (UAL) session.


## -parameters




### -param Data [in]

A pointer to an <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure that specifies session information.

Only the <b>RoleGuid</b> property of the <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure is required. All other members can be null.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/C7A0340F-3250-4570-9672-FC78AFC9ECC6">UalInstrument</a>



<a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a>
 

 

