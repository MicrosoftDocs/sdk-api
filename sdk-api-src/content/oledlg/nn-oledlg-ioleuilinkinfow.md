---
UID: NN:oledlg.IOleUILinkInfoW
title: IOleUILinkInfoW
author: windows-sdk-content
description: An extension of the IOleUILinkContainer interface. It returns the time that an object was last updated, which is link information that IOleUILinkContainer does not provide.
old-location: com\ioleuilinkinfo.htm
tech.root: com
ms.assetid: aadac00b-47bb-42eb-8458-b23867f6b975
ms.author: windowssdkdev
ms.date: 10/01/2018
ms.keywords: IOleUILinkInfo, IOleUILinkInfo interface [COM], IOleUILinkInfo interface [COM],described, IOleUILinkInfoA, IOleUILinkInfoW, _ole_IOleUILinkInfo, com.ioleuilinkinfo, oledlg/IOleUILinkInfo
ms.prod: windows
ms.technology: windows-sdk
ms.topic: interface
req.header: oledlg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
 - OleDlg.h
api_name:
 - IOleUILinkInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOleUILinkInfoW interface


## -description


An extension of the <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a> interface. It returns the time that an object was last updated, which is link information that <b>IOleUILinkContainer</b> does not provide.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOleUILinkInfo</b> interface inherits from <a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>. <b>IOleUILinkInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IOleUILinkInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/651dcfbc-577b-45a2-bf73-148a6f1c7030">GetLastUpdate</a>
</td>
<td align="left" width="63%">
Determines the last time the object was updated.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/7fc0aab3-7476-49ec-8a1d-3f4851f9f31c">IOleUILinkContainer</a>
 

 

