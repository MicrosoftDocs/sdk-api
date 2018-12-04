---
UID: NF:ual.UalStop
title: UalStop function
author: windows-sdk-content
description: Stops a User Access Logging (UAL) session.
old-location: ual\ualstop.htm
tech.root: ual
ms.assetid: 142A0C96-2D53-4C31-9847-D6D5313C841E
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: UalStop, UalStop function [User Access Logging], ual.ualstop, ual/UalStop
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
req.lib: Ualapi.lib
req.dll: Ualapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ualapi.dll
api_name:
 - UalStop
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# UalStop function


## -description


Stops a User Access Logging (UAL) session.


## -parameters




### -param Data [in]

A pointer to an <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure that specifies session information.

Only the <b>RoleGuid</b> property of the <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure is required. All other members can be null.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/C7A0340F-3250-4570-9672-FC78AFC9ECC6">UalInstrument</a>



<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>
 

 

