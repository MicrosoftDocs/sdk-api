---
UID: NF:mobsync.ISyncMgrSynchronizeCallback.LogError
title: ISyncMgrSynchronizeCallback::LogError
author: windows-sdk-content
description: Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.
old-location: shell\syncmgr_isyncmgrsynchronizecallback_logerror.htm
old-project: shell
ms.assetid: 7c25ef21-9815-41ad-bcc0-b41a62dc0fe5
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: ISyncMgrSynchronizeCallback interface [Windows Shell],LogError method, ISyncMgrSynchronizeCallback.LogError, ISyncMgrSynchronizeCallback::LogError, LogError, LogError method [Windows Shell], LogError method [Windows Shell],ISyncMgrSynchronizeCallback interface, mobsync/ISyncMgrSynchronizeCallback::LogError, shell.syncmgr_isyncmgrsynchronizecallback_logerror, syncmgr.isyncmgrsynchronizecallback_logerror
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.typenames: SYNCMGRSTATUS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronizeCallback.LogError
product: Windows
targetos: Windows
req.lib: 
req.dll: Mobsync.dll
req.irql: 
req.product: GDI+ 1.1
---

# ISyncMgrSynchronizeCallback::LogError


## -description


Called by a registered application to log information, warning, or an error message into the error tab on the synchronization manager status dialog box.


## -parameters




### -param dwErrorLevel [in]

Type: <b>DWORD</b>

The error level. Values are taken from the <a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a> enumeration.


### -param pszErrorText [in]

Type: <b>LPCWSTR</b>

A pointer to error text to be displayed in the error tab.


### -param pSyncLogError [in]

Type: <b>const <a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a> structure that contains additional error information. Registered applications that do not provide this data can pass <b>NULL</b>.


## -returns



Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and  the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The error information is logged successfully.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/1c817a21-be91-43af-86c8-aa7909ae2fa2">ISyncMgrSynchronizeCallback</a>



<a href="https://msdn.microsoft.com/0220792c-90e7-4802-9ba3-3fc6ce01e4de">SYNCMGRLOGERRORINFO</a>



<a href="https://msdn.microsoft.com/df3c3300-e203-4664-b8d5-9dc4835b33d8">SYNCMGRLOGLEVEL</a>
 

 

