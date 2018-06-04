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

# IVssSnapshotMgmt2::GetMinDiffAreaSize


## -description


Returns the current minimum size of the shadow copy storage area.


## -parameters




### -param pllMinDiffAreaSize [out]

A pointer to a variable that receives the minimum size, in bytes, of the shadow copy storage area.


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The shadow copy storage area minimum size is a per-computer setting that is specified by the <b>MinDiffAreaFileSize</b> registry key. For more information, see the entry for <b>MinDiffAreaFileSize</b> in <a href="https://msdn.microsoft.com/83449f78-cca1-449b-8c5f-3c8a91c8b3e7">Registry Keys and Values for Backup and Restore</a>.




## -see-also




<a href="https://msdn.microsoft.com/92c8c960-d548-4a44-8b10-b6180c974473">IVssSnapshotMgmt2</a>
 

 

