---
UID: NF:pla.IDataCollectorSet.get_RootPath
title: IDataCollectorSet::get_RootPath
author: windows-sdk-content
description: Retrieves or sets the base path where the subdirectories are created.
old-location: pla\idatacollectorset_get_rootpath.htm
tech.root: PLA
ms.assetid: 42940cec-c76a-433c-9308-f030dacb05a4
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: IDataCollectorSet interface [PLA],RootPath property, IDataCollectorSet.RootPath, IDataCollectorSet.get_RootPath, IDataCollectorSet::RootPath, IDataCollectorSet::get_RootPath, IDataCollectorSet::put_RootPath, RootPath property [PLA], RootPath property [PLA],IDataCollectorSet interface, base.idatacollectorset_get_rootpath, get_RootPath, pla.idatacollectorset_get_rootpath, pla/IDataCollectorSet::RootPath, pla/IDataCollectorSet::get_RootPath, pla/IDataCollectorSet::put_RootPath
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
 - IDataCollectorSet.RootPath
 - IDataCollectorSet.get_RootPath
 - IDataCollectorSet.put_RootPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDataCollectorSet::get_RootPath


## -description


Retrieves or sets the base path where the subdirectories are created.
<div class="alert"><b>Warning</b>  If you change the <b>RootPath</b> property, you should change it to a directory that only contains performance logs. Setting this to another directory, such as the drive root or system root, may cause files to be inadvertently deleted when the logs are cleaned up by the system.</div><div> </div>This property is read/write.


## -parameters


## -remarks



If this property is changed from the default value, the specified directory must exist before the <a href="https://msdn.microsoft.com/63f0c7b7-0dc6-4491-a2f5-eaae9d22da61">IDataCollectorSet::Start</a> method is called.




## -see-also




<a href="https://msdn.microsoft.com/a4ae0874-4ee6-46a1-9811-8cd4be26859c">IDataCollectorSet</a>



<a href="https://msdn.microsoft.com/c0047144-5f99-4acd-ad96-054afcbe6eb9">IDataCollectorSet::LatestOutputLocation</a>



<a href="https://msdn.microsoft.com/d0ca2655-f65a-4bcb-8e9e-f247b4207e56">IDataCollectorSet::OutputLocation</a>



<a href="https://msdn.microsoft.com/c2c55fd9-3b29-46be-9792-acb095b1c0e4">IDataCollectorSet::Subdirectory</a>
 

 

