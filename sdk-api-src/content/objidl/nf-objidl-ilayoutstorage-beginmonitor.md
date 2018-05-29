---
UID: NF:objidl.ILayoutStorage.BeginMonitor
title: ILayoutStorage::BeginMonitor
author: windows-sdk-content
description: The BeginMonitor method is used to begin monitoring when a loading operation is started. When the operation is complete, the application must call ILayoutStorage::EndMonitor.
old-location: stg\ilayoutstorage_beginmonitor.htm
old-project: Stg
ms.assetid: 16371d6c-adb9-43c2-80a4-377e94854bbb
ms.author: windowssdkdev
ms.date: 05/22/2018
ms.keywords: BeginMonitor, BeginMonitor method [Structured Storage], BeginMonitor method [Structured Storage],ILayoutStorage interface, ILayoutStorage interface [Structured Storage],BeginMonitor method, ILayoutStorage.BeginMonitor, ILayoutStorage::BeginMonitor, _stg_ilayoutstorage_beginmonitor, objidl/ILayoutStorage::BeginMonitor, stg.ilayoutstorage_beginmonitor
ms.prod: windows
ms.technology: windows-sdk
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
-	ILayoutStorage.BeginMonitor
product: Windows
targetos: Windows
req.lib: Uuid.lib
req.dll: Ole32.dll
req.irql: 
req.product: Rights Management Services client 1.0 or later
---

# ILayoutStorage::BeginMonitor


## -description



			The <b>BeginMonitor</b> method is used to begin monitoring when a loading operation is started. When the operation is complete, the application must call 
<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a>.


## -parameters






## -returns




						This method supports the standard return values E_OUTOFMEMORY, E_UNEXPECTED, E_INVALIDARG, and E_FAIL, as well as the following:




## -remarks



Normally an application calls 
<b>BeginMonitor</b> before the actual loading begins. Once this method has been called, the compound file implementation regards any operation performed on the files storages and streams as part of the desired access pattern. The result is a layout script like that created explicitly by calling 
<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>.

Applications will usually use monitoring to obtain the access pattern of embedded objects. Monitoring also makes possible generic layout tools,  that launch existing applications and monitor their access patterns.

A call to 
<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a> ends monitoring. Multiple calls to 
<b>BeginMonitor</b> and
<b>EndMonitor</b> are permitted. Monitoring can also be mixed with calls to 
<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>.




## -see-also




<a href="https://msdn.microsoft.com/83b9486b-78b6-473c-9a9a-33f470a4d70f">ILayoutStorage::EndMonitor</a>



<a href="https://msdn.microsoft.com/22ae3485-15d9-47e4-988e-fb760e67595b">ILayoutStorage::LayoutScript</a>
 

 

