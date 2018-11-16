---
UID: NF:pla.IDataCollectorSet.put_Subdirectory
title: IDataCollectorSet::put_Subdirectory
author: windows-sdk-content
description: Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set will write its logs.
old-location: pla\idatacollectorset_get_subdirectory.htm
tech.root: PLA
ms.assetid: c2c55fd9-3b29-46be-9792-acb095b1c0e4
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IDataCollectorSet interface [PLA],Subdirectory property, IDataCollectorSet.Subdirectory, IDataCollectorSet.put_Subdirectory, IDataCollectorSet::Subdirectory, IDataCollectorSet::get_Subdirectory, IDataCollectorSet::put_Subdirectory, Subdirectory property [PLA], Subdirectory property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_subdirectory, pla.idatacollectorset_get_subdirectory, pla/IDataCollectorSet::Subdirectory, pla/IDataCollectorSet::get_Subdirectory, pla/IDataCollectorSet::put_Subdirectory, put_Subdirectory
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: Pla.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Pla.dll
api_name:
 - IDataCollectorSet.Subdirectory
 - IDataCollectorSet.get_Subdirectory
 - IDataCollectorSet.put_Subdirectory
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- pla.h
: 
- IDataCollectorSet.put_Subdirectory
: 
---

# IDataCollectorSet::put_Subdirectory


## -description


Retrieves or sets a base subdirectory of the root path where the next instance of the data collector set will write its logs.

This property is read/write.


## -parameters


## -remarks



The actual name of the subdirectory used can be different if you had previously specified formatting options in the <a href="https://msdn.microsoft.com/f9e6eb88-ac38-4b99-ab64-a408f75f7969">IDataCollectorSet::SubdirectoryFormat</a> property. The <a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">IDataCollectorSet::LatestOutputLocation</a> property contains the actual folder name used. 

If a location is not specified, files are written to the path specified in the <a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a> property.

PLA creates the folders in the subdirectory path if they do not exist. Note that the folders will not inherit the ACLs from the root path. The user specified in the <a href="https://msdn.microsoft.com/32fe1dcf-9682-40fd-b301-45385fa33cbe">IDataCollectorSet::UserAccount</a> property and those in the Administrators group will have read and write access to the folders. Users in the Performance Log Users group and Performance Monitor Users group have read-only access.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">IDataCollectorSet::LatestOutputLocation</a>



<a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">IDataCollectorSet::OutputLocation</a>



<a href="https://msdn.microsoft.com/42940cec-c76a-433c-9308-f030dacb05a4">IDataCollectorSet::RootPath</a>



<a href="https://msdn.microsoft.com/f9e6eb88-ac38-4b99-ab64-a408f75f7969">IDataCollectorSet::SubdirectoryFormat</a>



<a href="https://msdn.microsoft.com/83b7df10-8b00-4d64-bf71-2c68e037ab3f">IDataCollectorSet::SubdirectoryFormatPattern</a>
 

 

