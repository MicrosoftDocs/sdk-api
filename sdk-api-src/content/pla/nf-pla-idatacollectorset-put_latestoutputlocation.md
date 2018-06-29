---
UID: NF:pla.IDataCollectorSet.put_LatestOutputLocation
title: IDataCollectorSet::put_LatestOutputLocation
author: windows-sdk-content
description: Retrieves or sets the fully decorated folder name that PLA used the last time logs were written.
old-location: pla\idatacollectorset_get_latestoutputlocation.htm
old-project: PLA
ms.assetid: c0047144-5f99-4acd-ad96-054afcbe6eb9
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IDataCollectorSet interface [PLA],LatestOutputLocation property, IDataCollectorSet.LatestOutputLocation, IDataCollectorSet.put_LatestOutputLocation, IDataCollectorSet::LatestOutputLocation, IDataCollectorSet::get_LatestOutputLocation, IDataCollectorSet::put_LatestOutputLocation, LatestOutputLocation property [PLA], LatestOutputLocation property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_latestoutputlocation, pla.idatacollectorset_get_latestoutputlocation, pla/IDataCollectorSet::LatestOutputLocation, pla/IDataCollectorSet::get_LatestOutputLocation, pla/IDataCollectorSet::put_LatestOutputLocation, put_LatestOutputLocation
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: pla.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: FolderActionSteps
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.LatestOutputLocation
 - IDataCollectorSet.get_LatestOutputLocation
 - IDataCollectorSet.put_LatestOutputLocation
product: Windows
targetos: Windows
req.lib: 
req.dll: Pla.dll
req.irql: 
req.product: ADAM
---

# IDataCollectorSet::put_LatestOutputLocation


## -description


Retrieves or sets the fully decorated folder name that PLA used the last time logs were written.

This property is read/write.


## -parameters


## -remarks



Typically, you do not set this property. When the data collector starts, PLA sets this property using the value from the <a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">IDataCollectorSet::OutputLocation</a> property.

You can set this property to empty if the folder has been deleted.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">IDataCollectorSet::OutputLocation</a>



<a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a>



<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a>
 

 

