---
UID: NN:cscobj.IOfflineFilesProgress
title: IOfflineFilesProgress (cscobj.h)
description: Used to report progress back to callers of lengthy Offline Files operations.helpviewer_keywords: ["IOfflineFilesProgress","IOfflineFilesProgress interface [Offline Files]","IOfflineFilesProgress interface [Offline Files]","described","cscobj/IOfflineFilesProgress","of.iofflinefilesprogress"]
old-location: of\iofflinefilesprogress.htm
tech.root: offlinefiles
ms.assetid: b568a8c6-119b-486e-94e3-fe4e54a395bb
ms.date: 12/05/2018
ms.keywords: IOfflineFilesProgress, IOfflineFilesProgress interface [Offline Files], IOfflineFilesProgress interface [Offline Files],described, cscobj/IOfflineFilesProgress, of.iofflinefilesprogress
f1_keywords:
- cscobj/IOfflineFilesProgress
dev_langs:
- c++
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
- IOfflineFilesProgress
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesProgress interface


## -description


Used to report progress back to callers of lengthy Offline Files operations. This interface provides the most basic "begin" and "end" notifications.  It is used as a base interface for all other progress interfaces.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesProgress</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesProgress</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesProgress</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-begin">Begin</a>
</td>
<td align="left" width="63%">
Reports that an operation has begun.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-end">End</a>
</td>
<td align="left" width="63%">
Reports that an operation has ended.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesprogress-queryabort">QueryAbort</a>
</td>
<td align="left" width="63%">
May be called during lengthy operations to determine if the operation should be canceled.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

