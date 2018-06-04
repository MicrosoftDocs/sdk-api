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

# ISharingConfigurationManager::GetSharePermissions


## -description


Gets the access permissions currently associated with the <b>User</b> or <b>Public</b> folder for the <i>Everyone</i> access control entry (ACE).


## -parameters




### -param dsid [in]

Type: <b><a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a></b>

One of the <a href="https://msdn.microsoft.com/02d3b664-eeef-4214-99e8-246241103c4e">DEF_SHARE_ID</a> values that specifies the folder.


### -param pRole [out]

Type: <b><a href="https://msdn.microsoft.com/d1c8764d-002e-4fbd-a0a6-1f469f8b1fbb">SHARE_ROLE</a>*</b>

A pointer to a value that, when this method returns successfully, receives one of the <a href="https://msdn.microsoft.com/d1c8764d-002e-4fbd-a0a6-1f469f8b1fbb">SHARE_ROLE</a> values that indicate the sharing permissions set for the folder specified in the <i>dsid</i> parameter.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



