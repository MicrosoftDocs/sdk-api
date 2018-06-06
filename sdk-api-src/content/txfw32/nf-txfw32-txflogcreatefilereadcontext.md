---
UID: NF:txfw32.TxfLogCreateFileReadContext
title: TxfLogCreateFileReadContext function
author: windows-sdk-content
description: Creates a context to be used to read replication records.
old-location: fs\txflogcreatefilereadcontext.htm
old-project: FileIO
ms.assetid: 57218f53-adcd-4a9a-b772-d3dab576b8c1
ms.author: windowssdkdev
ms.date: 05/16/2018
ms.keywords: TxfLogCreateFileReadContext, TxfLogCreateFileReadContext function [Files], fs.txflogcreatefilereadcontext, txfw32/TxfLogCreateFileReadContext
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
 - TxfLogCreateFileReadContext
product: Windows
targetos: Windows
req.lib: TxfW32.lib
req.dll: TxfW32.dll
req.irql: 
req.product: Windows XP with SP1 and later
---

# TxfLogCreateFileReadContext function


## -description


<p class="CCE_Message">[Microsoft strongly recommends developers utilize alternative means to achieve your 
    application’s needs. Many scenarios that TxF was developed for can be achieved through simpler and more readily 
    available techniques. Furthermore, TxF may not be available in future versions of Microsoft Windows. For more 
    information, and alternatives to TxF, please see 
    <a href="https://msdn.microsoft.com/9ee26e7e-990e-4cd3-8180-f0fcaac2b752">Alternatives to using Transactional NTFS</a>.]

Creates a context to be used to read replication records.


## -parameters




### -param LogPath [in]

The path that identifies the Resource Manager's .blf file.


### -param BeginningLsn [in]

The first LSN in the range to be read.


### -param EndingLsn

TBD


### -param TxfFileId [in]

The TxF identifier to search for in the LSN range. For more information, see <a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>.


### -param TxfLogContext [out]

A pointer to the context created.


#### - EndingLSN [in]

The last LSN in the range to be read.


## -returns



If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call 
       <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>.




## -see-also




<a href="https://msdn.microsoft.com/b7bdb226-69ce-4226-b826-baf9c732ec52">TXF_ID</a>



<a href="https://msdn.microsoft.com/e1f323bd-48cb-4264-89a0-185d18881726">TxfLogDestroyReadContext</a>
 

 

