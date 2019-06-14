---
UID: NN:infotech.IITWordWheel
title: IITWordWheel (infotech.h)
author: windows-sdk-content
description: Use this interface to perform word wheel keyword lookups. The Lookup method offers several ways of performing a search:\_it returns either an exact match, or the closest approximation based on a given prefix.
old-location: htmlhelp\iitwordwheel.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheelinterface.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IITWordWheel, IITWordWheel interface [HTML Help Workshop], IITWordWheel interface [HTML Help Workshop],described, htmlhelp.iitwordwheel, infotech/IITWordWheel, refIITWordWheelInterface
ms.topic: interface
req.header: infotech.h
req.include-header: 
req.target-type: Windows
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITWordWheel
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IITWordWheel interface


## -description


Use this interface to perform word wheel keyword lookups. The <b>Lookup</b> method offers several ways of performing a search: it returns either an exact match, or the closest approximation based on a given prefix.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITWordWheel</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IITWordWheel</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITWordWheel</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitwordwheel-close">Close</a>
</td>
<td align="left" width="63%">
Closes a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitwordwheel-count">Count</a>
</td>
<td align="left" width="63%">
Returns the number of entries in a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/infotech/nf-infotech-iitwordwheel-lookup(long_iitresultset_long)">Lookup(LONG,IITResultSet,LONG)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents as a result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitwordwheel-lookup(long_iitresultset_long)">Lookup(LONG,LPVOID,DWORD)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents in a buffer.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/infotech/nf-infotech-iitwordwheel-lookup(lpcvoid_bool_long)">Lookup(LPCVOID,BOOL,LONG)</a>
</td>
<td align="left" width="63%">
Returns the word wheel entry that is closest to the specified prefix.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitwordwheel-open">Open</a>
</td>
<td align="left" width="63%">
Opens a word wheel.



</td>
</tr>
</table> 

