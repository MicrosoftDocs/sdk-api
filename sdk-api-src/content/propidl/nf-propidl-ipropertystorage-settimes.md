---
UID: NF:propidl.IPropertyStorage.SetTimes
title: IPropertyStorage::SetTimes
author: windows-sdk-content
description: The SetTimes method sets the modification, access, and creation times of this property set, if supported by the implementation. Not all implementations support all these time values.
old-location: stg\ipropertystorage_settimes.htm
tech.root: Stg
ms.assetid: 23c7040a-e648-4898-806d-ad01d7027cc6
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IPropertyStorage interface [Structured Storage],SetTimes method, IPropertyStorage.SetTimes, IPropertyStorage::SetTimes, SetTimes, SetTimes method [Structured Storage], SetTimes method [Structured Storage],IPropertyStorage interface, _stg_ipropertystorage_settimes, propidl/IPropertyStorage::SetTimes, stg.ipropertystorage_settimes
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propidl.h
req.include-header: Objbase.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Ole32.dll
api_name:
 - IPropertyStorage.SetTimes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propidl.h
: 
- IPropertyStorage.SetTimes
: 
---

# IPropertyStorage::SetTimes


## -description


The <b>SetTimes</b> method sets the modification, access, and creation times of this property set, if supported by the implementation. Not all implementations support all these time values.


## -parameters




### -param pctime [in]

Pointer to the new creation time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


### -param patime [in]

Pointer to the new access time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


### -param pmtime [in]

Pointer to the new modification time for the property set. May be <b>NULL</b>, indicating that this time is not to be modified by this call.


## -returns



This method supports the standard return value E_UNEXPECTED, in addition to the following:




## -remarks



Sets the modification, access, and creation times of the current open property set, if supported by the implementation (not all implementations support all these time values). Unsupported time stamps are always reported as zero, enabling the caller to test for support. A call to <a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a> supplies (among other data) time-stamp information.

Notice that this functionality is provided as an 
<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a> method on a property-storage object that is already open, in contrast to being provided as a method in 
<a href="https://msdn.microsoft.com/0ea3e1e0-c135-4138-81e4-f72412fc3128">IPropertySetStorage</a>. Normally, when the 
<b>SetTimes</b> method is not explicitly called, the access and modification times are updated as a side effect of reading and writing the property set. When 
 <b>SetTimes</b>is used, the latest specified times supersede either default times or time values specified in previous calls to 
<b>SetTimes</b>.




## -see-also




<a href="https://msdn.microsoft.com/9baf8a0e-59e3-4fbd-9616-2ec9161520d1">FILETIME</a>



<a href="https://msdn.microsoft.com/c021f695-db54-4861-9f30-35a81d2dccd5">IPropertyStorage</a>



<a href="https://msdn.microsoft.com/46985c49-cb9b-4f67-8dff-e6fad9e188da">IPropertyStorage::Stat</a>
 

 

