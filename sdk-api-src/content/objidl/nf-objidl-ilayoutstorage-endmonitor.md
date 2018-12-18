---
UID: NF:objidl.ILayoutStorage.EndMonitor
title: ILayoutStorage::EndMonitor
author: windows-sdk-content
description: The EndMonitor method ends monitoring of a compound file. Must be preceded by a call to ILayoutStorage::BeginMonitor.
old-location: stg\ilayoutstorage_endmonitor.htm
tech.root: stg
ms.assetid: 83b9486b-78b6-473c-9a9a-33f470a4d70f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: EndMonitor, EndMonitor method [Structured Storage], EndMonitor method [Structured Storage],ILayoutStorage interface, ILayoutStorage interface [Structured Storage],EndMonitor method, ILayoutStorage.EndMonitor, ILayoutStorage::EndMonitor, _stg_ilayoutstorage_endmonitor, objidl/ILayoutStorage::EndMonitor, stg.ilayoutstorage_endmonitor
ms.topic: method
req.header: objidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps \| UWP apps]
req.target-min-winversvr: Windows 2000 Server [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Objidl.idl
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
 - ILayoutStorage.EndMonitor
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ILayoutStorage::EndMonitor


## -description


The <b>EndMonitor</b> method ends monitoring of a compound file. Must be preceded by a call to 
<a href="https://msdn.microsoft.com/16371d6c-adb9-43c2-80a4-377e94854bbb">ILayoutStorage::BeginMonitor</a>.


## -parameters






## -returns



This function supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as all return values for <a href="https://msdn.microsoft.com/9b84891d-62ca-4ddc-97b7-c4c79482abd9">CloseHandle</a>.




## -remarks



A call to 
<b>EndMonitor</b> is generally followed by a call to 
<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::RelayoutDocfile</a>, which uses the access pattern detected by the monitoring to restructure the compound file.




## -see-also




<a href="https://msdn.microsoft.com/16371d6c-adb9-43c2-80a4-377e94854bbb">ILayoutStorage::BeginMonitor</a>



<a href="https://msdn.microsoft.com/5db3a26c-595a-4c9b-bb6d-b170eb9864df">ILayoutStorage::ReLayoutDocfile</a>
 

 

