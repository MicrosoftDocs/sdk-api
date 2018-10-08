---
UID: NF:mmc.IStringTable.Enumerate
title: IStringTable::Enumerate
author: windows-sdk-content
description: Supplies a pointer to an IEnumString interface on an enumerator that can return the strings in a snap-in's string table.
old-location: mmc\istringtable_enumerate.htm
tech.root: mmc
ms.assetid: 3d23e29d-a80f-4710-8285-c9e64fd580a1
ms.author: windowssdkdev
ms.date: 10/05/2018
ms.keywords: Enumerate, Enumerate method [MMC], Enumerate method [MMC],IStringTable interface, IStringTable interface [MMC],Enumerate method, IStringTable.Enumerate, IStringTable::Enumerate, _slate_istringtable_enumerate, mmc.istringtable_enumerate, mmc/IStringTable::Enumerate
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
 - IStringTable.Enumerate
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IStringTable::Enumerate


## -description


The <b>IStringTable::Enumerate</b> method supplies a pointer to an <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface on an enumerator that can return the strings in a snap-in's string table. The <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> interface is a standard COM interface.


## -parameters




### -param ppEnum [out]

The address of <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a>* pointer variable that receives the interface pointer to the enumerator. If an error occurs, *<i>ppEnum</i> is set to <b>NULL</b>. If *<i>ppEnum </i>is non-<b>NULL</b>, MMC's implementation of <b>IEnumString</b> calls <a href="https://msdn.microsoft.com/b4316efd-73d4-4995-b898-8025a316ba63">IUnknown::AddRef</a> on the *<i>ppEnum</i>. The snap-in must call <a href="https://msdn.microsoft.com/4b494c6f-f0ee-4c35-ae45-ed956f40dc7a">IUnknown::Release</a> when the interface is no longer required.


## -returns



This method can return one of these values.




## -remarks



The returned <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> enumeration represents a snapshot of the collection of strings in the underlying string table the time that the enumeration was retrieved. Neither <a href="https://msdn.microsoft.com/6f134738-b5ed-4f45-bf91-eeb28c8965c6">IEnumString::Reset</a>, nor IEnumString::Clone takes a new snapshot of the collection.

The implementation of <a href="https://msdn.microsoft.com/7f3e642a-17c7-4646-8c70-da6b0946a415">IEnumString</a> uses the default OLE task memory allocator to allocate memory for the strings it returns.




## -see-also




<a href="https://msdn.microsoft.com/3b4cfc92-4f50-4b62-bb2c-77c8e0e003da">IStringTable</a>



<a href="https://msdn.microsoft.com/c239618d-ed27-4d73-9e88-7323960a0e68">IStringTable::FindString</a>
 

 

