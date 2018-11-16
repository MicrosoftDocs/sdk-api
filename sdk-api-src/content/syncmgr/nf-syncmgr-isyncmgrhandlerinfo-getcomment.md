---
UID: NF:syncmgr.ISyncMgrHandlerInfo.GetComment
title: ISyncMgrHandlerInfo::GetComment
author: windows-sdk-content
description: Gets a string that contains commentary regarding the handler.
old-location: shell\ISyncMgrHandlerInfo_GetComment.htm
tech.root: shell
ms.assetid: 755d3038-934f-42b7-a807-7037fa0ea21e
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: GetComment, GetComment method [Windows Shell], GetComment method [Windows Shell],ISyncMgrHandlerInfo interface, ISyncMgrHandlerInfo interface [Windows Shell],GetComment method, ISyncMgrHandlerInfo.GetComment, ISyncMgrHandlerInfo::GetComment, _shell_ISyncMgrHandlerInfo_GetComment, shell.ISyncMgrHandlerInfo_GetComment, syncmgr/ISyncMgrHandlerInfo::GetComment
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandlerInfo.GetComment
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- syncmgr.h
: 
- ISyncMgrHandlerInfo.GetComment
: 
---

# ISyncMgrHandlerInfo::GetComment


## -description


Gets a string that contains commentary regarding the handler.


## -parameters




### -param ppszComment [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the comment string. This string is of maximum length MAX_SYNCMGR_NAME including the terminating null character.


## -returns



Type: <b>HRESULT</b>

Returns S_OK if successful, or an error value otherwise. If the method fails, <i>ppszComment</i> contains an empty string.




## -remarks



This string could be provided by a handler to display a summary of contents of the partnership, for instance "32 contacts" or "13 songs". The string can have a maximum length of MAX_SYNCMGR_NAME including the terminating null character.

The comment value is displayed as the System.Sync.Comments (PKEY_Sync_Comments) property in the folder UI when a synchronization is not being performed.

Sync Center calls this method whenever the <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> method is called.

The handler is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.



