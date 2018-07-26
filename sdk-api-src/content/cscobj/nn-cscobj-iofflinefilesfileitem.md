---
UID: NN:cscobj.IOfflineFilesFileItem
title: IOfflineFilesFileItem
author: windows-sdk-content
description: Represents a file item in the Offline Files cache.
old-location: of\iofflinefilesfileitem.htm
old-project: offlinefiles
ms.assetid: 53b9af4b-7526-4b54-bae2-61c97aa67ebf
ms.author: windowssdkdev
ms.date: 07/23/2018
ms.keywords: IOfflineFilesFileItem, IOfflineFilesFileItem interface [Offline Files], IOfflineFilesFileItem interface [Offline Files],described, cscobj/IOfflineFilesFileItem, of.iofflinefilesfileitem
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesFileItem
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesFileItem interface


## -description


Represents a file item in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesFileItem</b> interface inherits from <a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>. <b>IOfflineFilesFileItem</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesFileItem</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f4ef4836-378c-4a9b-a805-e576d4637a2a">IsEncrypted</a>
</td>
<td align="left" width="63%">
Determines whether an item in the Offline Files cache is encrypted.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/6f731b25-f4f0-4635-af00-dbd1ba4e5f11">IsSparse</a>
</td>
<td align="left" width="63%">
Determines whether an item in the Offline Files cache is sparsely cached.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/870cf4c4-e757-429d-b6cc-c136ed5aa10e">IOfflineFilesItem</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

