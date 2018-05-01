---
UID: NF:objidl.IStorage.Revert
title: IStorage::Revert method
author: windows-driver-content
description: The Revert method discards all changes that have been made to the storage object since the last commit operation.
old-location: stg\istorage_revert.htm
old-project: Stg
ms.assetid: d1b7626e-bad1-47b5-8bcd-3da3b05c53c4
ms.author: windowsdriverdev
ms.date: 4/20/2018
ms.keywords: IStorage, IStorage interface [Structured Storage], Revert method, IStorage::Revert, Revert method [Structured Storage], Revert method [Structured Storage], IStorage interface, Revert,IStorage.Revert, _stg_istorage_revert, objidl/IStorage::Revert, stg.istorage_revert
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps | UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: THDTYPE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Ole32.dll
api_name:
-	IStorage.Revert
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStorage::Revert method


## -description


The <b>Revert</b> method discards all changes that have been made to the storage object since the last commit operation.


## -parameters






## -returns



This method can return one of these values.




## -remarks



For storage objects opened in transacted mode, the <b>IStorage::Revert</b> method discards any uncommitted changes to this storage object or changes that have been committed to this storage object from nested elements.

After this method returns, any existing elements (substorages or streams) that were opened from the reverted storage object are invalid and can no longer be used. Specifying these reverted elements in any call except <a href="_com_iunknown_release">IUnknown::Release</a> returns the error STG_E_REVERTED

This method has no effect on storage objects opened in direct mode.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/72831f2c-1e07-429b-af4c-2aaced3f3888">IStorage::Commit</a>
 

 

