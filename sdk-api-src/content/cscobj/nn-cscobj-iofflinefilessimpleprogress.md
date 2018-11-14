---
UID: NN:cscobj.IOfflineFilesSimpleProgress
title: IOfflineFilesSimpleProgress
author: windows-sdk-content
description: Used to report progress back to callers of lengthy Offline Files operations.
old-location: of\iofflinefilessimpleprogress.htm
tech.root: OfflineFiles
ms.assetid: 490f0958-125b-4c09-8ca4-07532ed8d4d4
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IOfflineFilesSimpleProgress, IOfflineFilesSimpleProgress interface [Offline Files], IOfflineFilesSimpleProgress interface [Offline Files],described, cscobj/IOfflineFilesSimpleProgress, of.iofflinefilessimpleprogress
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesSimpleProgress
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesSimpleProgress interface


## -description


Used to report progress back to callers of lengthy Offline Files operations.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesSimpleProgress</b> interface inherits from <a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>. <b>IOfflineFilesSimpleProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesSimpleProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/0e3496ee-e987-4c37-93ff-bc8409acabde">ItemBegin</a>
</td>
<td align="left" width="63%">
Reports that an operation on an item is beginning.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/60ed3b12-b56e-4a58-8e37-a4a745ddb783">ItemResult</a>
</td>
<td align="left" width="63%">
Reports that an item has been processed during the operation.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/b568a8c6-119b-486e-94e3-fe4e54a395bb">IOfflineFilesProgress</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

