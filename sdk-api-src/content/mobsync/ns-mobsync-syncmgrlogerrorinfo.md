---
UID: NS:mobsync._tagSYNCMGRLOGERRORINFO
title: SYNCMGRLOGERRORINFO (mobsync.h)
author: windows-sdk-content
description: Provides error information for use in the ISyncMgrSynchronizeCallback::LogError method.
old-location: shell\syncmgr_syncmgrlogerrorinfo.htm
tech.root: shell
ms.assetid: 0220792c-90e7-4802-9ba3-3fc6ce01e4de
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: "*LPSYNCMGRLOGERRORINFO, LPSYNCMGRLOGERRORINFO, LPSYNCMGRLOGERRORINFO structure pointer [Windows Shell], SYNCMGRERRORFLAG_ENABLEJUMPTEXT, SYNCMGRLOGERRORINFO, SYNCMGRLOGERRORINFO structure [Windows Shell], SYNCMGRLOGERROR_ERRORFLAGS, SYNCMGRLOGERROR_ERRORID, SYNCMGRLOGERROR_ITEMID, mobsync/LPSYNCMGRLOGERRORINFO, mobsync/SYNCMGRLOGERRORINFO, shell.syncmgr_syncmgrlogerrorinfo, syncmgr.syncmgrlogerrorinfo"
ms.topic: struct
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Mobsync.h
api_name:
 - SYNCMGRLOGERRORINFO
product: Windows
targetos: Windows
req.typenames: SYNCMGRLOGERRORINFO, *LPSYNCMGRLOGERRORINFO
req.redist: 
---

# SYNCMGRLOGERRORINFO structure


## -description


Provides error information for use in the <a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a> method.


## -struct-fields




### -field cbSize

Type: <b>DWORD</b>

The size of the structure.


### -field mask

Type: <b>DWORD</b>

The mask value. The synchronization manager handler implemented by your application can set any combination of the following bits to indicate which fields of <b>SYNCMGRLOGERRORINFO</b> it has filled in when calling <a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a>.



#### SYNCMGRLOGERROR_ERRORFLAGS

The <b>dwSyncMgrErrorFlags</b> field is valid.



#### SYNCMGRLOGERROR_ERRORID

The <b>ErrorID</b> field is valid.



#### SYNCMGRLOGERROR_ITEMID

The <b>ItemID</b> field is valid.


### -field dwSyncMgrErrorFlags

Type: <b>DWORD</b>

Error flags. At this time only the following value is recognized.



#### SYNCMGRERRORFLAG_ENABLEJUMPTEXT

The <a href="https://msdn.microsoft.com/0e313c61-6482-4396-b4b8-824fba0226ac">ISyncMgrSynchronize::ShowError</a> method should be called on this item.


### -field ErrorID

Type: <b>GUID</b>

An error identifier.


### -field ItemID

Type: <b>GUID</b>

The item where the error occurred.


## -see-also




<a href="https://msdn.microsoft.com/7c25ef21-9815-41ad-bcc0-b41a62dc0fe5">ISyncMgrSynchronizeCallback::LogError</a>
 

 

