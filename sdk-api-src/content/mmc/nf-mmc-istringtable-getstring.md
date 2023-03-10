---
UID: NF:mmc.IStringTable.GetString
title: IStringTable::GetString (mmc.h)
description: Enables a snap-in to retrieve a string from the snap-in's string table.
helpviewer_keywords: ["GetString","GetString method [MMC]","GetString method [MMC]","IStringTable interface","IStringTable interface [MMC]","GetString method","IStringTable.GetString","IStringTable::GetString","_slate_istringtable_getstring","mmc.istringtable_getstring","mmc/IStringTable::GetString"]
old-location: mmc\istringtable_getstring.htm
tech.root: mmc
ms.assetid: 34dbf92a-b54d-4f60-87ff-493c9946a57d
ms.date: 12/05/2018
ms.keywords: GetString, GetString method [MMC], GetString method [MMC],IStringTable interface, IStringTable interface [MMC],GetString method, IStringTable.GetString, IStringTable::GetString, _slate_istringtable_getstring, mmc.istringtable_getstring, mmc/IStringTable::GetString
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
 - IStringTable::GetString
 - mmc/IStringTable::GetString
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
 - IStringTable.GetString
---

# IStringTable::GetString


## -description

The <b>IStringTable::GetString</b> method enables a snap-in to retrieve a string from the snap-in's string table.

## -parameters

### -param StringID [in]

The ID of the string to be retrieved from the snap-in's string table.

### -param cchBuffer [in]

The number of characters in lpBuffer.

### -param lpBuffer [out]

A pointer  to the buffer for the character string.

### -param pcchOut [out]

The number of characters in the retrieved string, not including the NULL terminator. If the number of characters written is not required, pass <b>NULL</b> for this parameter.

## -returns

This method can return one of these values.

## -remarks

If lpBuffer is not large enough to hold the entire string corresponding to StringID, as much of the string as will fit is copied to the buffer and is null-terminated.

## -see-also

<a href="/windows/desktop/api/mmc/nn-mmc-istringtable">IStringTable</a>



<a href="/windows/desktop/api/mmc/nf-mmc-istringtable-getstringlength">IStringTable::GetStringLength</a>