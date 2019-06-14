---
UID: NN:winsync.ISyncSessionExtendedErrorInfo
title: ISyncSessionExtendedErrorInfo (winsync.h)
author: windows-sdk-content
description: Represents information about which provider caused synchronization to fail.
old-location: winsync\isyncsessionextendederrorinfo.htm
tech.root: winsync
ms.assetid: 0c6f90af-f4ca-4fa9-8050-acc61b4ee8d2
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncSessionExtendedErrorInfo, ISyncSessionExtendedErrorInfo interface [Windows Sync], ISyncSessionExtendedErrorInfo interface [Windows Sync],described, winsync.isyncsessionextendederrorinfo, winsync/ISyncSessionExtendedErrorInfo
ms.topic: interface
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
 - winsync.h
api_name:
 - ISyncSessionExtendedErrorInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncSessionExtendedErrorInfo interface


## -description


Represents information about which provider caused synchronization to fail.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncSessionExtendedErrorInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncSessionExtendedErrorInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncSessionExtendedErrorInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncsessionextendederrorinfo-getsyncproviderwitherror">GetSyncProviderWithError</a>
</td>
<td align="left" width="63%">
Gets the <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncprovider">ISyncProvider</a> interface of the provider that caused synchronization to fail.

</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

