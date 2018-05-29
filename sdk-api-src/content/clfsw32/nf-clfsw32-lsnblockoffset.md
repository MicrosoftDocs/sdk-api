---
UID: NF:clfsw32.LsnBlockOffset
title: LsnBlockOffset function
author: windows-sdk-content
description: Returns the sector-aligned block offset that is contained in the specified LSN.
old-location: fs\lsnblockoffset.htm
old-project: Clfs
ms.assetid: 72445d03-1b9a-48a6-993e-792e1f524f4b
ms.author: windowssdkdev
ms.date: 05/10/2018
ms.keywords: LsnBlockOffset, LsnBlockOffset function [Files], clfsw32/LsnBlockOffset, fs.lsnblockoffset
ms.prod: windows
ms.technology: windows-sdk
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
req.typenames: LOG_MANAGEMENT_CALLBACKS, *PLOG_MANAGEMENT_CALLBACKS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Clfsw32.dll
api_name:
-	LsnBlockOffset
product: Windows
targetos: Windows
req.lib: Clfsw32.lib
req.dll: Clfsw32.dll
req.irql: 
---

# LsnBlockOffset function


## -description


Returns the sector-aligned block offset that is contained in the specified LSN.


## -parameters




### -param plsn [in]

A pointer to a <a href="https://msdn.microsoft.com/library/windows/hardware/ff541824">CLFS_LSN</a> structure from which the block offset is to be retrieved.


## -returns



<b>LsnBlockOffset</b> returns the block offset that is contained in <i>plsn</i>.




## -remarks



The block offset that is returned by this function is a multiple of the sector size on the stable storage medium. For example, if the sector size is 1024 bytes, the block offset is a multiple of 1024.


#### Examples

For an example that uses this function, see <a href="https://msdn.microsoft.com/dc7e204c-201d-4a84-9a87-576c73627f67">Enumerating Log Containers</a>.

<div class="code"></div>



## -see-also




<a href="https://msdn.microsoft.com/1bbbb37b-8197-44bd-b19b-c43ece1c46d2">LsnContainer</a>



<a href="https://msdn.microsoft.com/3662ac53-25d5-4d8c-8f98-02f313e03dce">LsnCreate</a>



<a href="https://msdn.microsoft.com/90aa2df8-328d-404c-a145-ad500a6e611a">LsnRecordSequence</a>
 

 

