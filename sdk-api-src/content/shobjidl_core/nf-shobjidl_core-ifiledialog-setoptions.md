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

# IFileDialog::SetOptions


## -description


Sets flags to control the behavior of the dialog.


## -parameters




### -param fos [in]

Type: <b>FILEOPENDIALOGOPTIONS</b>

One or more of the <a href="https://msdn.microsoft.com/CDDB4B39-AFB9-4C0D-9D5A-0F2EA9EABE64">FILEOPENDIALOGOPTIONS</a> values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Generally, this method should take the value that was retrieved by <a href="https://msdn.microsoft.com/8a01b64d-b58e-4470-a5ed-8cf821b26c6b">IFileDialog::GetOptions</a> and modify it to include or exclude options by setting the appropriate flags.



