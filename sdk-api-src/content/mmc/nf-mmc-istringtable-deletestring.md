---
UID: NF:mmc.IStringTable.DeleteString
title: IStringTable::DeleteString
author: windows-sdk-content
description: Enables a snap-in to delete a specified string from the snap-in string table.
old-location: mmc\istringtable_deletestring.htm
tech.root: mmc
ms.assetid: 57d04890-5dd8-45e5-9b46-b982ea3a4f36
ms.author: windowssdkdev
ms.date: 09/04/2018
ms.keywords: DeleteString, DeleteString method [MMC], DeleteString method [MMC],IStringTable interface, IStringTable interface [MMC],DeleteString method, IStringTable.DeleteString, IStringTable::DeleteString, _slate_istringtable_deletestring, mmc.istringtable_deletestring, mmc/IStringTable::DeleteString
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
 - IStringTable.DeleteString
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStringTable::DeleteString


## -description


The <b>IStringTable::DeleteString</b> method enables a snap-in to delete a specified string from the snap-in string table.


## -parameters




### -param StringID [in]

The string to be deleted from the snap-in string table.


## -returns



This method can return one of these values.




## -remarks



Strings in the string table are reference counted. For example, adding the string "My Text" to the string table will return an ID, such as 1234. Adding "My Text" to the string table a second time will return an ID of 1234 again, and the internal reference count for the string will be incremented. Two calls to <b>IStringTable::DeleteString</b> will be required to completely remove "My Text" from the snap-in string table.




## -see-also




<a href="https://msdn.microsoft.com/3b4cfc92-4f50-4b62-bb2c-77c8e0e003da">IStringTable</a>



<a href="https://msdn.microsoft.com/fd4672fb-89d1-4542-b917-58c01290c928">IStringTable::AddString</a>



<a href="https://msdn.microsoft.com/9a0b02f6-3c15-4687-a1b8-2beba40dd1dc">IStringTable::DeleteAllStrings</a>
 

 

