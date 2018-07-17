---
UID: NF:syncmgr.ISyncMgrEvent.GetLinkText
title: ISyncMgrEvent::GetLinkText
author: windows-sdk-content
description: Gets the text for the hot link for the event.
old-location: shell\ISyncMgrEvent_GetLinkText.htm
old-project: shell
ms.assetid: f8a7226b-270e-495e-a43f-8e6a9c7a77df
ms.author: windowssdkdev
ms.date: 07/13/2018
ms.keywords: GetLinkText, GetLinkText method [Windows Shell], GetLinkText method [Windows Shell],ISyncMgrEvent interface, ISyncMgrEvent interface [Windows Shell],GetLinkText method, ISyncMgrEvent.GetLinkText, ISyncMgrEvent::GetLinkText, _shell_ISyncMgrEvent_GetLinkText, shell.ISyncMgrEvent_GetLinkText, syncmgr/ISyncMgrEvent::GetLinkText
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrEvent.GetLinkText
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEvent::GetLinkText


## -description


Gets the text for the hot link for the event. The hot link is a displayed property that the user can click to execute an action. This allows the handler to show an available action that the user can see at a glance in the folder. The link text is the text that is displayed to the user.


## -parameters




### -param ppszLinkText [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to the link text as a Unicode string.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The event is expected to allocate the string buffer using <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>, which Sync Center uses to deallocate the string buffer.



