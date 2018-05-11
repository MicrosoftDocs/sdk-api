---
UID: NF:objidl.IStorage.SetElementTimes
title: IStorage::SetElementTimes
author: windows-driver-content
description: The SetElementTimes method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.
old-location: stg\istorage_setelementtimes.htm
old-project: Stg
ms.assetid: f6a1fba4-0444-4de3-a838-2d339878fe24
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: IStorage interface [Structured Storage],SetElementTimes method, IStorage.SetElementTimes, IStorage::SetElementTimes, SetElementTimes, SetElementTimes method [Structured Storage], SetElementTimes method [Structured Storage],IStorage interface, _stg_istorage_setelementtimes, objidl/IStorage::SetElementTimes, stg.istorage_setelementtimes
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
-	IStorage.SetElementTimes
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IStorage::SetElementTimes


## -description


The <b>SetElementTimes</b>  method sets the modification, access, and creation times of the specified storage element, if the underlying file system supports this method.


## -parameters




### -param pwcsName [in]

The name of the storage object element whose times are to be modified. If <b>NULL</b>, the time is set on the root storage rather than one of its elements.


### -param pctime [in]

Either the new creation time for the element or <b>NULL</b> if the creation time is not to be modified.


### -param patime [in]

Either the new access time for the element or <b>NULL</b> if the access time is not to be modified.


### -param pmtime [in]

Either the new modification time for the element or <b>NULL</b> if the modification time is not to be modified.


## -returns



This method can return one of these values.




## -remarks



<b>SetElementTimes</b>  sets time statistics for the specified storage element within this storage object.

Not all file systems support all the time values. This method sets those times that are supported and ignores the rest. Each time-value parameter can be <b>NULL</b>; indicating that no modification should occur.

Call the 
<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a> method to retrieve these time values.




## -see-also




<a href="https://msdn.microsoft.com/2a2253f6-d3d3-403e-a9ba-53a541c7a31e">IStorage - Compound File Implementation</a>



<a href="https://msdn.microsoft.com/87478fa8-1b5f-44ed-bffc-e139c7f44a12">IStorage::Stat</a>
 

 

