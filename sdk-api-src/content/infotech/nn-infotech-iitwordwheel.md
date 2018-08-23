---
UID: NN:infotech.IITWordWheel
title: IITWordWheel
author: windows-sdk-content
description: Use this interface to perform word wheel keyword lookups. The Lookup method offers several ways of performing a search:\_it returns either an exact match, or the closest approximation based on a given prefix.
old-location: htmlhelp\iitwordwheel.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitwordwheelinterface.htm
ms.author: windowssdkdev
ms.date: 02/15/2018
ms.keywords: IITWordWheel, IITWordWheel interface [HTML Help Workshop], IITWordWheel interface [HTML Help Workshop],described, htmlhelp.iitwordwheel, infotech/IITWordWheel, refIITWordWheelInterface
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: infotech.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
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
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITWordWheel interface


## -description


Use this interface to perform word wheel keyword lookups. The <b>Lookup</b> method offers several ways of performing a search: it returns either an exact match, or the closest approximation based on a given prefix.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITWordWheel</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IITWordWheel</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/en-us/library/ms670055(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670056(v=VS.85).aspx">Count</a>
</td>
<td align="left" width="63%">
Returns the number of entries in a word wheel.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670060(v=VS.85).aspx">Lookup(,IITResultSet,)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents as a result set.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670059(v=VS.85).aspx">Lookup(,LPVOID,DWORD)</a>
</td>
<td align="left" width="63%">
Looks up an entry and returns contents in a buffer.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670058(v=VS.85).aspx">Lookup(LPCVOID,BOOL,)</a>
</td>
<td align="left" width="63%">
Returns the word wheel entry that is closest to the specified prefix.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670061(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens a word wheel.



</td>
</tr>
</table> 

