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

# ISearchManager::GetIndexerVersionStr


## -description


Retrieves the version of the current indexer as a single string.


## -parameters




### -param ppszVersionString [out]

Type: <b>LPWSTR*</b>

Receives the version of the current indexer.



##### 65 on Windows XP/Windows Server 2003

02.06.5000.5378



##### 66 on Windows XP/Windows Server 2003

02.06.6000.5414



##### 0 on Windows XP/Windows Server 2003

03.00.5824.280



##### 01 on Windows XP/Windows Server 2003

03.01.6000.72



#### Windows Search on Windows Vista RTM/Windows Server RTM

03.00.6000.16386



#### Windows Search on Windows Vista SP1/Windows Server 2008

03.00.6001.18000



##### 0 Preview on all platforms

04.00.6001.381



##### 0 on all platforms

04.00.6001.16503


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ReindexMatchingUrls code sample, available on <a href="http://go.microsoft.com/fwlink/p/?linkid=155654">Code Gallery</a> and the <a href="http://go.microsoft.com/fwlink/p/?linkid=129787">Windows 7 SDK</a>, demonstrates ways to specify which files to re-index and how.



