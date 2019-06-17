---
UID: NF:txfw32.TxfLogDestroyReadContext
title: TxfLogDestroyReadContext function (txfw32.h)
author: windows-sdk-content
description: Closes a read context created by the TxfLogCreateFileReadContext function.
old-location: fs\txflogdestroyreadcontext.htm
tech.root: FileIO
ms.assetid: e1f323bd-48cb-4264-89a0-185d18881726
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: TxfLogDestroyReadContext, TxfLogDestroyReadContext function [Files], fs.txflogdestroyreadcontext, txfw32/TxfLogDestroyReadContext
ms.topic: function
f1_keywords: ["txfw32/TxfLogDestroyReadContext"]
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
req.lib: TxfW32.lib
req.dll: TxfW32.dll
req.irql: 
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
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# TxfLogDestroyReadContext function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://docs.microsoft.com/windows/desktop/FileIO/deprecation-of-txf">Alternatives to using Transactional NTFS</a>.]

Closes a read context created by the 
    <a href="https://docs.microsoft.com/windows/desktop/api/txfw32/nf-txfw32-txflogcreatefilereadcontext">TxfLogCreateFileReadContext</a> function.


## -parameters




### -param TxfLogContext [in]

A pointer to the context.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://docs.microsoft.com/windows/desktop/api/errhandlingapi/nf-errhandlingapi-getlasterror">GetLastError</a>.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/txfw32/nf-txfw32-txflogcreatefilereadcontext">TxfLogCreateFileReadContext</a>
 

 

