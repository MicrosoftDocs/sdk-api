---
UID: NF:clfsw32.AdvanceLogBase
title: AdvanceLogBase function
author: windows-sdk-content
description: Advances the base log sequence number (LSN) of a log stream to the specified LSN.
old-location: fs\advancelogbase.htm
tech.root: Clfs
ms.assetid: aecdea3b-ac42-43d4-88b3-14cd810a4017
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: AdvanceLogBase, AdvanceLogBase function [Files], clfsw32/AdvanceLogBase, fs.advancelogbase
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: clfsw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Clfsw32.dll
api_name:
 - AdvanceLogBase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# AdvanceLogBase function


## -description


 Advances the base log sequence number (LSN) of a log stream to the   specified LSN.


## -parameters




### -param pvMarshal [in, out]

A pointer to the marshaling context  that  a successful call to  <a href="https://msdn.microsoft.com/750c0615-bfac-402b-a590-6c9d800cf2d8">CreateLogMarshallingArea</a> returns.


### -param plsnBase [in]

The new base LSN for the log that is specified in <i>pvMarshal</i>.  

This LSN must be in the range between the current base LSN and the last LSN of the log, inclusively.


### -param fFlags [in]

This parameter is not implemented at this time, and must be zero.


### -param pOverlapped [in, out, optional]

A pointer to an <a href="https://msdn.microsoft.com/5037f6b9-e316-483b-a8e2-b58d2587ebd9">OVERLAPPED</a> structure that is required for asynchronous operation. 

If asynchronous operation is not used, this parameter can be <b>NULL</b>.


## -returns



If the function succeeds, the return value is nonzero.
						

If the function fails, the return value is zero. To get extended error information, call 
<a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.

The following list identifies the possible error codes:




## -remarks



<b>AdvanceLogBase</b> might flush data and metadata when it is called.




## -see-also




<a href="https://msdn.microsoft.com/2e47a5c9-a0bd-4cd1-ba30-9ebde6df0f91">Obtaining the Next LSN</a>
 

 

