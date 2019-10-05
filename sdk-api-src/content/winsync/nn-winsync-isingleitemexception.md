---
UID: NN:winsync.ISingleItemException
title: ISingleItemException (winsync.h)
author: windows-sdk-content
description: Represents an item to exclude from a knowledge object.
old-location: winsync\isingleitemexception.htm
tech.root: winsync
ms.assetid: 623553cb-9dc2-4504-9c49-357a0526b130
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISingleItemException, ISingleItemException interface [Windows Sync], ISingleItemException interface [Windows Sync],described, winsync.isingleitemexception, winsync/ISingleItemException
ms.topic: interface
f1_keywords: 
 - "winsync/ISingleItemException"
dev_langs:
 - c++
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
 - ISingleItemException
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISingleItemException interface


## -description


Represents an item to exclude from a knowledge object. 


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISingleItemException</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISingleItemException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISingleItemException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isingleitemexception-getclockvector">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with the item exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isingleitemexception-getitemid">GetItemId</a>
</td>
<td align="left" width="63%">
Gets the ID of the item that is specified in the exception.


</td>
</tr>
</table> 


## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

