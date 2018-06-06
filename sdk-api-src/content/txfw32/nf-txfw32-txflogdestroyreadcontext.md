---
UID: NF:txfw32.TxfLogDestroyReadContext
title: TxfLogDestroyReadContext function
author: windows-sdk-content
description: Closes a read context created by the TxfLogCreateFileReadContext function.
old-location: fs\txflogdestroyreadcontext.htm
old-project: FileIO
ms.assetid: e1f323bd-48cb-4264-89a0-185d18881726
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: TxfLogDestroyReadContext, TxfLogDestroyReadContext function [Files], fs.txflogdestroyreadcontext, txfw32/TxfLogDestroyReadContext
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: txfw32.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1 [desktop apps only]
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
tech.root: 
req.typenames: EnTvRat_US_TV
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - TxfW32.dll
api_name:
 - TxfLogDestroyReadContext
product: Windows
targetos: Windows
req.lib: TxfW32.lib
req.dll: TxfW32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TxfLogDestroyReadContext function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Closes a read context created by the 
    <a href="https://msdn.microsoft.com/57218f53-adcd-4a9a-b772-d3dab576b8c1">TxfLogCreateFileReadContext</a> function.


## -parameters




### -param TxfLogContext [in]

A pointer to the context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/57218f53-adcd-4a9a-b772-d3dab576b8c1">TxfLogCreateFileReadContext</a>
 

 

