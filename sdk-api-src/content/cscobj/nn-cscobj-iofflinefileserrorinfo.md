---
UID: NN:cscobj.IOfflineFilesErrorInfo
title: IOfflineFilesErrorInfo (cscobj.h)
author: windows-sdk-content
description: Provides a text description and raw data block associated with an error.
old-location: of\iofflinefileserrorinfo.htm
tech.root: offlinefiles
ms.assetid: 6c78d475-aa63-49e4-863f-1a197801f2f9
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesErrorInfo, IOfflineFilesErrorInfo interface [Offline Files], IOfflineFilesErrorInfo interface [Offline Files],described, cscobj/IOfflineFilesErrorInfo, of.iofflinefileserrorinfo
ms.topic: interface
f1_keywords: 
 - "cscobj/IOfflineFilesErrorInfo"
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
 - IOfflineFilesErrorInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesErrorInfo interface


## -description


Provides a text description and raw data block associated with an error.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileserrorinfo-getdescription">GetDescription</a>
</td>
<td align="left" width="63%">
Retrieves a text string describing the error.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefileserrorinfo-getrawdata">GetRawData</a>
</td>
<td align="left" width="63%">
Retrieves a block of bytes containing internal data associated with the error.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

