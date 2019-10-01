---
UID: NN:winsync.ISyncSessionState2
title: ISyncSessionState2 (winsync.h)
author: windows-sdk-content
description: Represents additional information about the current synchronization session.
old-location: winsync\isyncsessionstate2.htm
tech.root: winsync
ms.assetid: c98e675f-48f4-4ffa-bc81-18a58edd8c34
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncSessionState2, ISyncSessionState2 interface [Windows Sync], ISyncSessionState2 interface [Windows Sync],described, winsync.isyncsessionstate2, winsync/ISyncSessionState2
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncSessionState2"
req.header: winsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Winsync.h
api_name:
 - ISyncSessionState2
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncSessionState2 interface


## -description


Represents additional information about the current synchronization session.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncSessionState2</b> interface inherits from <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState</a>. <b>ISyncSessionState2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncSessionState2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate2-getsessionerrorstatus">GetSessionErrorStatus</a>
</td>
<td align="left" width="63%">
Gets the error value that indicates why the synchronization session failed.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionstate2-setproviderwitherror">SetProviderWithError</a>
</td>
<td align="left" width="63%">
Indicates which provider caused synchronization to fail.


</td>
</tr>
</table> 


## -remarks



An <b>ISyncSessionState2</b> object can be obtained by passing <b>IID_ISyncSessionState2</b> to the <b>QueryInterface</b> method of an <b>ISyncSessionState</b> object.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncsessionstate">ISyncSessionState Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

