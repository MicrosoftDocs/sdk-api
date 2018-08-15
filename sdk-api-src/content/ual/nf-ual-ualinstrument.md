---
UID: NF:ual.UalInstrument
title: UalInstrument function
author: windows-sdk-content
description: Records the specified data to the User Access Logging (UAL) framework by using information from a UAL_DATA_BLOB structure.
old-location: ual\ualinstrument.htm
old-project: ual
ms.assetid: C7A0340F-3250-4570-9672-FC78AFC9ECC6
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: UalInstrument, UalInstrument function [User Access Logging], ual.ualinstrument, ual/UalInstrument
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: ual.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: RECORD_READING_POLICY
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Ualapi.dll
api_name:
 - UalInstrument
product: Windows
targetos: Windows
req.lib: Ualapi.lib
req.dll: Ualapi.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# UalInstrument function


## -description


Records the specified data to the  User Access Logging (UAL) framework by using information from a <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure.

You must call the <a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a> function before calling the <b>UalInstrument</b> function. When you have finished calling this function, call the <a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a> function to clean up resources.


## -parameters




### -param Data [in]

A pointer to a <a href="https://msdn.microsoft.com/5C191327-0D15-41D7-8218-73F387740FDF">UAL_DATA_BLOB</a> structure that specifies session information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/800E8BCF-39A1-490A-9B6A-12EE900B8D17">UalStart</a>



<a href="https://msdn.microsoft.com/142A0C96-2D53-4C31-9847-D6D5313C841E">UalStop</a>
 

 

