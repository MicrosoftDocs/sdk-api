---
UID: NS:mmc._RDCITEMHDR
title: "_RDCITEMHDR"
author: windows-sdk-content
description: The RDITEMHDR structure is introduced in MMC 1.2.
old-location: mmc\rditemhdr.htm
old-project: MMC
ms.assetid: 35feb978-3859-423d-ac33-711b242ab939
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: RDITEMHDR, RDITEMHDR structure [MMC], _RDCITEMHDR, _slate_rditemhdr, mmc.rditemhdr, mmc/RDITEMHDR
ms.prod: windows
ms.technology: windows-sdk
ms.topic: struct
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: RDITEMHDR
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RDITEMHDR
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# _RDCITEMHDR structure


## -description


The 
<b>RDITEMHDR</b> structure is introduced in MMC 1.2.

The 
<b>RDITEMHDR</b> structure is used by the 
<a href="https://msdn.microsoft.com/78f0648b-1d1b-4786-89fa-ef51b7743a2d">RDCOMPARE</a> structure to specify the type and cookie value of a scope or result item.


## -struct-fields




### -field dwFlags

A value that specifies whether the item is a scope or result item. If the <b>RDCI_ScopeItem</b> (0x80000000) flag is set, the item is a scope item. Otherwise, the item is a result item.


### -field cookie

The unique identifier of the scope or result item object to be compared as part of the sorting operation.


### -field lpReserved

Reserved for future use.


## -remarks



If the snap-in implements the 
<a href="https://msdn.microsoft.com/e4b305e4-4649-42f4-86f4-3c12e5aa5337">IResultDataCompareEx</a> interface, MMC allocates an 
<a href="https://msdn.microsoft.com/78f0648b-1d1b-4786-89fa-ef51b7743a2d">RDCOMPARE</a> structure and two 
<b>RDITEMHDR</b> structures and then calls the snap-ins 
<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a> method. After the method returns, MMC releases the three structures it allocated.




## -see-also




<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a>



<a href="https://msdn.microsoft.com/78f0648b-1d1b-4786-89fa-ef51b7743a2d">RDCOMPARE</a>
 

 

