---
UID: NS:mmc._RDCITEMHDR
title: RDITEMHDR (mmc.h)
description: The RDITEMHDR structure is introduced in MMC 1.2.
helpviewer_keywords: ["RDITEMHDR","RDITEMHDR structure [MMC]","_slate_rditemhdr","mmc.rditemhdr","mmc/RDITEMHDR"]
old-location: mmc\rditemhdr.htm
tech.root: mmc
ms.assetid: 35feb978-3859-423d-ac33-711b242ab939
ms.date: 12/05/2018
ms.keywords: RDITEMHDR, RDITEMHDR structure [MMC], _slate_rditemhdr, mmc.rditemhdr, mmc/RDITEMHDR
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
targetos: Windows
req.typenames: RDITEMHDR
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _RDCITEMHDR
 - mmc/_RDCITEMHDR
 - RDITEMHDR
 - mmc/RDITEMHDR
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mmc.h
api_name:
 - RDITEMHDR
---

# RDITEMHDR structure


## -description

The 
<b>RDITEMHDR</b> structure is introduced in MMC 1.2.

The 
<b>RDITEMHDR</b> structure is used by the 
<a href="/windows/desktop/api/mmc/ns-mmc-rdcompare">RDCOMPARE</a> structure to specify the type and cookie value of a scope or result item.

## -struct-fields

### -field dwFlags

A value that specifies whether the item is a scope or result item. If the <b>RDCI_ScopeItem</b> (0x80000000) flag is set, the item is a scope item. Otherwise, the item is a result item.

### -field cookie

The unique identifier of the scope or result item object to be compared as part of the sorting operation.

### -field lpReserved

Reserved for future use.

## -remarks

If the snap-in implements the 
<a href="/windows/desktop/api/mmc/nn-mmc-iresultdatacompareex">IResultDataCompareEx</a> interface, MMC allocates an 
<a href="/windows/desktop/api/mmc/ns-mmc-rdcompare">RDCOMPARE</a> structure and two 
<b>RDITEMHDR</b> structures and then calls the snap-ins 
<a href="/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a> method. After the method returns, MMC releases the three structures it allocated.

## -see-also

<a href="/windows/desktop/api/mmc/nf-mmc-iresultdatacompareex-compare">IResultDataCompareEx::Compare</a>



<a href="/windows/desktop/api/mmc/ns-mmc-rdcompare">RDCOMPARE</a>