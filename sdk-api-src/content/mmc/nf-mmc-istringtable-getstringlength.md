---
UID: NF:mmc.IStringTable.GetStringLength
title: IStringTable::GetStringLength
author: windows-sdk-content
description: Enables a snap-in to determine the length of a string in the snap-in's string table.
old-location: mmc\istringtable_getstringlength.htm
old-project: MMC
ms.assetid: 1924c4fa-ecbb-4f03-8c93-e2bb3dc8f4e3
ms.author: windowssdkdev
ms.date: 07/24/2018
ms.keywords: GetStringLength, GetStringLength method [MMC], GetStringLength method [MMC],IStringTable interface, IStringTable interface [MMC],GetStringLength method, IStringTable.GetStringLength, IStringTable::GetStringLength, _slate_istringtable_getstringlength, mmc.istringtable_getstringlength, mmc/IStringTable::GetStringLength
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmcndmgr.dll
api_name:
 - IStringTable.GetStringLength
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
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
<a href="https://msdn.microsoft.com/34dbf92a-b54d-4f60-87ff-493c9946a57d">IStringTable::GetString</a>.




## -see-also




<a href="https://msdn.microsoft.com/3b4cfc92-4f50-4b62-bb2c-77c8e0e003da">IStringTable</a>



<a href="https://msdn.microsoft.com/34dbf92a-b54d-4f60-87ff-493c9946a57d">IStringTable::GetString</a>
 

 

