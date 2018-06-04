---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# _tagSYNCMGRLOGERRORINFO structure


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
 

 

