---
UID: NN:cscobj.IOfflineFilesDirtyInfo
title: IOfflineFilesDirtyInfo (cscobj.h)
author: windows-sdk-content
description: Represents information about an unsynchronized (&#0034;dirty&#0034;) file in the Offline Files cache.
old-location: of\iofflinefilesdirtyinfo.htm
tech.root: offlinefiles
ms.assetid: 10414443-9e7f-4520-80dd-d2ad098c1d44
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesDirtyInfo, IOfflineFilesDirtyInfo interface [Offline Files], IOfflineFilesDirtyInfo interface [Offline Files],described, cscobj/IOfflineFilesDirtyInfo, of.iofflinefilesdirtyinfo
ms.topic: interface
f1_keywords: 
 - "cscobj/IOfflineFilesDirtyInfo"
dev_langs:
 - c++
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
 - IOfflineFilesDirtyInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesDirtyInfo interface


## -description


Represents information about an unsynchronized ("dirty") file in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesDirtyInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesDirtyInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesdirtyinfo-localdirtybytecount">LocalDirtyByteCount</a>
</td>
<td align="left" width="63%">
Retrieves the amount of unsynchronized data for a file in the local Offline Files cache.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesdirtyinfo-remotedirtybytecount">RemoteDirtyByteCount</a>
</td>
<td align="left" width="63%">
This method is reserved for future use.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nn-cscobj-iofflinefilesfileitem">IOfflineFilesFileItem</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

