---
UID: NF:mmc.IStringTable.GetString
title: IStringTable::GetString
author: windows-sdk-content
description: Enables a snap-in to retrieve a string from the snap-in's string table.
old-location: mmc\istringtable_getstring.htm
tech.root: MMC
ms.assetid: 34dbf92a-b54d-4f60-87ff-493c9946a57d
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetString, GetString method [MMC], GetString method [MMC],IStringTable interface, IStringTable interface [MMC],GetString method, IStringTable.GetString, IStringTable::GetString, _slate_istringtable_getstring, mmc.istringtable_getstring, mmc/IStringTable::GetString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
 - IStringTable.GetString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- mmc.h
: 
- IStringTable.GetString
: 
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




<a href="https://msdn.microsoft.com/3b4cfc92-4f50-4b62-bb2c-77c8e0e003da">IStringTable</a>



<a href="https://msdn.microsoft.com/1924c4fa-ecbb-4f03-8c93-e2bb3dc8f4e3">IStringTable::GetStringLength</a>
 

 

