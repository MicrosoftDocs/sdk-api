---
UID: NF:mmc.IStringTable.FindString
title: IStringTable::FindString (mmc.h)
description: Enables a snap-in to search for a string in the snap-in string table.
helpviewer_keywords: ["FindString","FindString method [MMC]","FindString method [MMC]","IStringTable interface","IStringTable interface [MMC]","FindString method","IStringTable.FindString","IStringTable::FindString","_slate_istringtable_findstring","mmc.istringtable_findstring","mmc/IStringTable::FindString"]
old-location: mmc\istringtable_findstring.htm
tech.root: mmc
ms.assetid: c239618d-ed27-4d73-9e88-7323960a0e68
ms.date: 12/05/2018
ms.keywords: FindString, FindString method [MMC], FindString method [MMC],IStringTable interface, IStringTable interface [MMC],FindString method, IStringTable.FindString, IStringTable::FindString, _slate_istringtable_findstring, mmc.istringtable_findstring, mmc/IStringTable::FindString
f1_keywords:
- mmc/IStringTable.FindString
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Mmcndmgr.dll
api_name:
- IStringTable.FindString
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IStringTable::FindString


## -description


The <b>IStringTable::FindString</b> method enables a snap-in to search for a string in the snap-in string table.


## -parameters




### -param pszFind [in]

The string to be searched for in the string table.


### -param pStringID [out]

A pointer to the ID of the string found in the string table.


## -returns



This method can return one of these values.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="https://docs.microsoft.com/windows/desktop/api/mmc/nf-mmc-istringtable-enumerate">IStringTable::Enumerate</a>
 

 

