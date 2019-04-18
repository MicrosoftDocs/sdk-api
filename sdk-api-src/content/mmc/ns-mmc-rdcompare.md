---
UID: NS:mmc._RDCOMPARE
title: RDCOMPARE (mmc.h)
author: windows-sdk-content
description: The RDCOMPARE structure is introduced in MMC 1.2.
old-location: mmc\rdcompare.htm
tech.root: mmc
ms.assetid: 78f0648b-1d1b-4786-89fa-ef51b7743a2d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: RDCOMPARE, RDCOMPARE structure [MMC], _slate_rdcompare, mmc.rdcompare, mmc/RDCOMPARE
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RDCOMPARE
product: Windows
targetos: Windows
req.typenames: RDCOMPARE
req.redist: 
ms.custom: 19H1
---

# RDCOMPARE structure


## -description


The 
<b>RDCOMPARE</b> structure is introduced in MMC 1.2.

The 
<b>RDCOMPARE</b> structure is used by the 
<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a> method for specifying information used for sorting scope and result items in the result pane of a primary snap-in.


## -struct-fields




### -field cbSize

Size of this structure.


### -field dwFlags

Reserved. Always zero.


### -field nColumn

Column being sorted.


### -field lUserParam

A value that specifies user-provided information that is passed into 
<a href="https://msdn.microsoft.com/457eccaf-3727-4b29-a38b-9f009749673e">IResultData::Sort</a>. MMC does not interpret this parameter.


### -field prdch1

A pointer to an 
<a href="https://msdn.microsoft.com/35feb978-3859-423d-ac33-711b242ab939">RDITEMHDR</a> structure that specifies the first item's type (scope or result) and cookie.


### -field prdch2

A pointer to an 
<a href="https://msdn.microsoft.com/35feb978-3859-423d-ac33-711b242ab939">RDITEMHDR</a> structure that specifies the second item's type (scope or result) and cookie.


## -remarks



If the snap-in implements the 
<a href="https://msdn.microsoft.com/e4b305e4-4649-42f4-86f4-3c12e5aa5337">IResultDataCompareEx</a> interface, MMC MMC allocates the parameters to the 
<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a> snap-in's method and then calls the method. MMC releases the parameters after the method returns.




## -see-also




<a href="https://msdn.microsoft.com/0e3a8094-0d09-4a9c-8211-a0eb6a89ad55">IResultDataCompareEx::Compare</a>



<a href="https://msdn.microsoft.com/35feb978-3859-423d-ac33-711b242ab939">RDITEMHDR</a>
 

 

