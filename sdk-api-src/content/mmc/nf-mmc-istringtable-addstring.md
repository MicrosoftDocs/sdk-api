---
UID: NF:mmc.IStringTable.AddString
title: IStringTable::AddString
author: windows-sdk-content
description: Enables a snap-in to add a string to the snap-in's string table.
old-location: mmc\istringtable_addstring.htm
old-project: mmc
ms.assetid: fd4672fb-89d1-4542-b917-58c01290c928
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: AddString, AddString method [MMC], AddString method [MMC],IStringTable interface, IStringTable interface [MMC],AddString method, IStringTable.AddString, IStringTable::AddString, _slate_istringtable_addstring, mmc.istringtable_addstring, mmc/IStringTable::AddString
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
 - IStringTable.AddString
product: Windows
targetos: Windows
req.lib: 
req.dll: Mmcndmgr.dll
req.irql: 
req.product: GDI+ 1.1
---

# IStringTable::AddString


## -description


The <b>IStringTable::AddString</b> method enables a snap-in to add a string to the snap-in's string table.


## -parameters




### -param pszAdd [in]

The string to add to the string table.


### -param pStringID [out]

A pointer to the ID of the string added to the string table.


## -returns



This method can return one of these values.




## -remarks



Strings in the string table are reference counted. For example, adding the string "My Text" to the string table will return an ID, say 1234. Adding "My Text" to the string table a second time will return an ID of 1234 again, and the internal reference count for the string will be incremented. Two calls to 
<a href="https://msdn.microsoft.com/57d04890-5dd8-45e5-9b46-b982ea3a4f36">IStringTable::DeleteString</a>, or a single call to 
<a href="https://msdn.microsoft.com/9a0b02f6-3c15-4687-a1b8-2beba40dd1dc">IStringTable::DeleteAllStrings</a>, will be required to completely remove "My Text" from the snap-in's string table.

<b>IStringTable::AddString</b> returns a nonzero string ID if the call to it was successful. Snap-ins therefore can safely use 0 to indicate an unassigned ID.




## -see-also




<a href="https://msdn.microsoft.com/3b4cfc92-4f50-4b62-bb2c-77c8e0e003da">IStringTable</a>



<a href="https://msdn.microsoft.com/9a0b02f6-3c15-4687-a1b8-2beba40dd1dc">IStringTable::DeleteAllStrings</a>



<a href="https://msdn.microsoft.com/57d04890-5dd8-45e5-9b46-b982ea3a4f36">IStringTable::DeleteString</a>
 

 

