---
UID: NF:clfsw32.LsnContainer
title: LsnContainer function
author: windows-sdk-content
description: Retrieves the logical container ID that is contained in a specified LSN.
old-location: fs\lsncontainer.htm
tech.root: Clfs
ms.assetid: 1bbbb37b-8197-44bd-b19b-c43ece1c46d2
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: LsnContainer, LsnContainer function [Files], clfsw32/LsnContainer, fs.lsncontainer
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
 - LsnContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# LsnContainer function


## -description


Retrieves the logical container ID that is contained in a specified LSN.


## -parameters




### -param plsn [in]

A pointer to a <a href="https://msdn.microsoft.com/f388feec-e1dc-4ae9-aa33-8f2fdc4dbc9a">CLFS_LSN</a> structure from which the container ID is to be retrieved.


## -returns



This function returns the logical container ID that is contained in <i>plsn</i>. The logical container ID is not necessarily the same as the ID of the physical container on stable storage.




## -see-also




<a href="https://msdn.microsoft.com/72445d03-1b9a-48a6-993e-792e1f524f4b">LsnBlockOffset</a>



<a href="https://msdn.microsoft.com/3662ac53-25d5-4d8c-8f98-02f313e03dce">LsnCreate</a>



<a href="https://msdn.microsoft.com/90aa2df8-328d-404c-a145-ad500a6e611a">LsnRecordSequence</a>
 

 

