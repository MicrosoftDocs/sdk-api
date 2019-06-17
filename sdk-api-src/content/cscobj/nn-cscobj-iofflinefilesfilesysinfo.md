---
UID: NN:cscobj.IOfflineFilesFileSysInfo
title: IOfflineFilesFileSysInfo (cscobj.h)
author: windows-sdk-content
description: Represents the standard information associated with a file system item in the Offline Files cache.
old-location: of\iofflinefilesfilesysinfo.htm
tech.root: offlinefiles
ms.assetid: d3da183d-eb12-4411-b461-b58689ef5bff
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IOfflineFilesFileSysInfo, IOfflineFilesFileSysInfo interface [Offline Files], IOfflineFilesFileSysInfo interface [Offline Files],described, cscobj/IOfflineFilesFileSysInfo, of.iofflinefilesfilesysinfo
ms.topic: interface
f1_keywords: ["cscobj/IOfflineFilesFileSysInfo"]
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
 - IOfflineFilesFileSysInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IOfflineFilesFileSysInfo interface


## -description


Represents the standard information associated with a file system item in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesFileSysInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IOfflineFilesFileSysInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesFileSysInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesfilesysinfo-getattributes">GetAttributes</a>
</td>
<td align="left" width="63%">
Retrieves the Win32 attributes for an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesfilesysinfo-getfilesize">GetFileSize</a>
</td>
<td align="left" width="63%">
Retrieves the size of an item.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/cscobj/nf-cscobj-iofflinefilesfilesysinfo-gettimes">GetTimes</a>
</td>
<td align="left" width="63%">
Retrieves the time values associated with an item.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/offlinefiles/offline-files-api-interfaces">Offline Files API Interfaces</a>
 

 

