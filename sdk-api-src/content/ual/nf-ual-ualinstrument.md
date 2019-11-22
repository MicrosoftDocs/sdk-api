---
UID: NF:ual.UalInstrument
title: UalInstrument function (ual.h)

description: Records the specified data to the User Access Logging (UAL) framework by using information from a UAL_DATA_BLOB structure.
old-location: ual\ualinstrument.htm
tech.root: ual
ms.assetid: C7A0340F-3250-4570-9672-FC78AFC9ECC6

ms.date: 12/05/2018
ms.keywords: UalInstrument, UalInstrument function [User Access Logging], ual.ualinstrument, ual/UalInstrument
ms.topic: function
f1_keywords: 
 - "ual/UalInstrument"
dev_langs:
 - c++
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
 - UalInstrument
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# UalInstrument function


## -description


Records the specified data to the  User Access Logging (UAL) framework by using information from a <a href="https://docs.microsoft.com/windows/desktop/api/ual/ns-ual-ual_data_blob">UAL_DATA_BLOB</a> structure.

You must call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ual/nf-ual-ualstart">UalStart</a> function before calling the <b>UalInstrument</b> function. When you have finished calling this function, call the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ual/nf-ual-ualstop">UalStop</a> function to clean up resources.


## -parameters




### -param Data [in]

A pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/ual/ns-ual-ual_data_blob">UAL_DATA_BLOB</a> structure that specifies session information.


## -returns



If the function succeeds, it returns <b>S_OK</b>. If it fails, it returns an error code.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ual/nf-ual-ualstart">UalStart</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/ual/nf-ual-ualstop">UalStop</a>
 

 

