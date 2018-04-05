---
UID: NF:syncmgr.ISyncMgrEvent.GetLinkReference
title: ISyncMgrEvent::GetLinkReference method
author: windows-driver-content
description: Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.
old-location: shell\ISyncMgrEvent_GetLinkReference.htm
old-project: shell
ms.assetid: de625328-59ba-4574-9b7b-3e8fc643c8ad
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: GetLinkReference method [Windows Shell], GetLinkReference method [Windows Shell], ISyncMgrEvent interface, GetLinkReference,ISyncMgrEvent.GetLinkReference, ISyncMgrEvent, ISyncMgrEvent interface [Windows Shell], GetLinkReference method, ISyncMgrEvent::GetLinkReference, _shell_ISyncMgrEvent_GetLinkReference, shell.ISyncMgrEvent_GetLinkReference, syncmgr/ISyncMgrEvent::GetLinkReference
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
-	ISyncMgrEvent.GetLinkReference
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetLinkReference method


## -description


Gets the reference for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder.


## -parameters




### -param ppszLinkReference [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a link reference as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The link reference is executed when the user clicks on the hot link. When the user clicks the link, Sync Center calls <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">GetObject</a>, requesting the SYNCMGR_OBJECTID_EventLinkClick object for the <a href="https://msdn.microsoft.com/53ea9488-77e0-4eb2-86d3-88747ba44654">ISyncMgrEventLinkUIOperation</a> interface. The object is initialized with an <a href="https://msdn.microsoft.com/fb9877fc-016c-472b-9af2-f2470c5c7e3b">ISyncMgrEvent</a> interface pointer that can be used by the <i>Run</i> method. If the handler does not support this object ID, Sync Center passes the link reference to <a href="https://msdn.microsoft.com/8b1f3978-a0ee-4684-8a37-98e270b63897">ShellExecute</a>.
            

The event is expected to allocate the string buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



