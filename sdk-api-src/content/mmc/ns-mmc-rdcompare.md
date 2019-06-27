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
f1_keywords: 
 - "mmc/RDCOMPARE"
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
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a> method for specifying information used for sorting scope and result items in the result pane of a primary snap-in.


## -struct-fields




### -field cbSize

Size of this structure.


### -field dwFlags

Reserved. Always zero.


### -field nColumn

Column being sorted.


### -field lUserParam

A value that specifies user-provided information that is passed into 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdata-sort">IResultData::Sort</a>. MMC does not interpret this parameter.


### -field prdch1

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_rdcitemhdr">RDITEMHDR</a> structure that specifies the first item's type (scope or result) and cookie.


### -field prdch2

A pointer to an 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_rdcitemhdr">RDITEMHDR</a> structure that specifies the second item's type (scope or result) and cookie.


## -remarks



If the snap-in implements the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interface, MMC MMC allocates the parameters to the 
<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a> snap-in's method and then calls the method. MMC releases the parameters after the method returns.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/ns-mmc-_rdcitemhdr">RDITEMHDR</a>
 

 

