---
UID: NF:shobjidl_core.ISharingConfigurationManager.DeleteShare
title: ISharingConfigurationManager::DeleteShare
author: windows-sdk-content
description: Removes sharing from either the Users or Public folder.
old-location: shell\ISharingConfigurationManager_DeleteShare.htm
old-project: shell
ms.assetid: 8b78d321-0da6-4b7e-8408-34784d309a1b
ms.author: windowssdkdev
ms.date: 05/24/2018
ms.keywords: DeleteShare, DeleteShare method [Windows Shell], DeleteShare method [Windows Shell],ISharingConfigurationManager interface, ISharingConfigurationManager interface [Windows Shell],DeleteShare method, ISharingConfigurationManager.DeleteShare, ISharingConfigurationManager::DeleteShare, _shell_ISharingConfigurationManager_DeleteShare, shell.ISharingConfigurationManager_DeleteShare, shobjidl_core/ISharingConfigurationManager::DeleteShare
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	shobjidl_core.h
api_name:
-	ISharingConfigurationManager.DeleteShare
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Outlook Express 6.0
---

# ISharingConfigurationManager::DeleteShare


## -description


Removes sharing from either the <b>Users</b> or <b>Public</b> folder.


## -parameters




### -param dsid [in]

Type: <b><a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a></b>

One of the <a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a> values that specifies the folder to no longer share.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Running this method requires an Administrator privilege level.



