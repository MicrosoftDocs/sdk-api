---
UID: NF:syncmgr.ISyncMgrEvent.GetName
title: ISyncMgrEvent::GetName method
author: windows-driver-content
description: Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.
old-location: shell\ISyncMgrEvent_GetName.htm
old-project: shell
ms.assetid: d533ab62-f6b2-4be9-ac58-98250d99a8c3
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetName method [Windows Shell], GetName method [Windows Shell], ISyncMgrEvent interface, GetName,ISyncMgrEvent.GetName, ISyncMgrEvent, ISyncMgrEvent interface [Windows Shell], GetName method, ISyncMgrEvent::GetName, _shell_ISyncMgrEvent_GetName, shell.ISyncMgrEvent_GetName, syncmgr/ISyncMgrEvent::GetName
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrEvent.GetName
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetName method


## -description


Gets the name of the event. This string can be a simple name for the event or a short summary. It is displayed in the folder and in the property sheet for the event.


## -parameters




### -param ppszName [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a name as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event is expected to allocate the string buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



