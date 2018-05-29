---
UID: NN:cscobj.IOfflineFilesDirtyInfo
title: IOfflineFilesDirtyInfo
author: windows-sdk-content
description: Represents information about an unsynchronized (&#0034;dirty&#0034;) file in the Offline Files cache.
old-location: of\iofflinefilesdirtyinfo.htm
old-project: OfflineFiles
ms.assetid: 10414443-9e7f-4520-80dd-d2ad098c1d44
ms.author: windowssdkdev
ms.date: 05/11/2018
ms.keywords: IOfflineFilesDirtyInfo, IOfflineFilesDirtyInfo interface [Offline Files], IOfflineFilesDirtyInfo interface [Offline Files],described, cscobj/IOfflineFilesDirtyInfo, of.iofflinefilesdirtyinfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista with SP1
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
req.typenames: OFFLINEFILES_SYNC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	CscSvc.dll
-	CscObj.dll
api_name:
-	IOfflineFilesDirtyInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
---

# IOfflineFilesDirtyInfo interface


## -description


Represents information about an unsynchronized ("dirty") file in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesDirtyInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IOfflineFilesDirtyInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesDirtyInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/c261d5ac-5834-42c7-b644-4244db9d653e">LocalDirtyByteCount</a>
</td>
<td align="left" width="63%">
Retrieves the amount of unsynchronized data for a file in the local Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/3913dc9d-f640-407d-b3b9-77b33f26e726">RemoteDirtyByteCount</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/53b9af4b-7526-4b54-bae2-61c97aa67ebf">IOfflineFilesFileItem</a>



<a href="https://msdn.microsoft.com/9dea396f-ab71-4b2e-b5d3-776c16614f26">Offline Files API Interfaces</a>
 

 

