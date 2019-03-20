---
UID: NF:cfapi.CfSetInSyncState
title: CfSetInSyncState function (cfapi.h)
author: windows-sdk-content
description: Sets the in-sync state for a placeholder file or folder.
old-location: cloudapi\cfsetinsyncstate.htm
tech.root: cfApi
ms.assetid: 1CB7955D-E530-4F34-8D67-BC608F8B6AF1
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CfSetInSyncState, CfSetInSyncState function, cfapi/CfSetInSyncState, cloudApi.cfsetinsyncstate
ms.topic: function
req.header: cfapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 10, version 1709 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: CldApi.lib
req.dll: CldApi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - CldApi.dll
api_name:
 - CfSetInSyncState
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# CfSetInSyncState function


## -description


Sets the in-sync state for a placeholder file or folder.


## -parameters




### -param FileHandle [in]

A handle to the placeholder.	The caller must have WRITE_DATA or WRITE_DAC access to the placeholder.


### -param InSyncState [in]

The in-sync state. See <a href="https://msdn.microsoft.com/05F99E47-00EE-422C-BDDF-CCCDDD4DADED">CF_IN_SYNC_STATE</a> for more details.


### -param InSyncFlags [in]

The in-sync state flags. See <a href="https://msdn.microsoft.com/55A20F07-0B3E-4C1D-9E59-288DAE08D134">CF_SET_IN_SYNC_FLAGS</a> for more details.


### -param InSyncUsn [in, out, optional]

When specified, this instructs the platform to only perform in-sync setting if the file still has the same USN value as the one passed in. Passing a pointer to a USN value of 0 on input is the same as passing a NULL pointer.  On return, this is the final USN value after setting the in-sync state.


## -returns



If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



