---
UID: NF:mmc.IStringTable.GetStringLength
title: IStringTable::GetStringLength (mmc.h)
description: Enables a snap-in to determine the length of a string in the snap-in's string table.
helpviewer_keywords: ["GetStringLength","GetStringLength method [MMC]","GetStringLength method [MMC]","IStringTable interface","IStringTable interface [MMC]","GetStringLength method","IStringTable.GetStringLength","IStringTable::GetStringLength","_slate_istringtable_getstringlength","mmc.istringtable_getstringlength","mmc/IStringTable::GetStringLength"]
old-location: mmc\istringtable_getstringlength.htm
tech.root: mmc
ms.assetid: 1924c4fa-ecbb-4f03-8c93-e2bb3dc8f4e3
ms.date: 12/05/2018
ms.keywords: GetStringLength, GetStringLength method [MMC], GetStringLength method [MMC],IStringTable interface, IStringTable interface [MMC],GetStringLength method, IStringTable.GetStringLength, IStringTable::GetStringLength, _slate_istringtable_getstringlength, mmc.istringtable_getstringlength, mmc/IStringTable::GetStringLength
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
req.dll: Mmcndmgr.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IStringTable::GetStringLength
 - mmc/IStringTable::GetStringLength
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IStringTable.GetStringLength
---

# IStringTable::GetStringLength


## -description

The <b>IStringTable::GetStringLength</b> method enables a snap-in to determine the length of a string in the snap-in's string table.

## -parameters

### -param StringID [in]

The identifier for the string whose length is being retrieved.

### -param pcchString [out]

The number of characters in the specified string in the snap-in's string table, not including the terminator.

## -returns

This method can return one of these values.

## -remarks

Use this method to determine the size of the buffer required for 
<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-getstring">IStringTable::GetString</a>.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-getstring">IStringTable::GetString</a>