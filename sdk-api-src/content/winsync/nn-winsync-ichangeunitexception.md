---
UID: NN:winsync.IChangeUnitException
title: IChangeUnitException (winsync.h)
description: Represents a change unit to exclude from a knowledge object.
helpviewer_keywords: ["IChangeUnitException","IChangeUnitException interface [Windows Sync]","IChangeUnitException interface [Windows Sync]","described","winsync.ichangeunitexception","winsync/IChangeUnitException"]
old-location: winsync\ichangeunitexception.htm
tech.root: winsync
ms.assetid: 3b47abab-0a33-405f-a765-307ab800bad6
ms.date: 12/05/2018
ms.keywords: IChangeUnitException, IChangeUnitException interface [Windows Sync], IChangeUnitException interface [Windows Sync],described, winsync.ichangeunitexception, winsync/IChangeUnitException
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IChangeUnitException
 - winsync/IChangeUnitException
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - winsync.h
api_name:
 - IChangeUnitException
---

# IChangeUnitException interface


## -description

Represents a change unit to exclude from a knowledge object.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IChangeUnitException</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IChangeUnitException</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IChangeUnitException</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitexception-getchangeunitid">GetChangeUnitId</a>
</td>
<td align="left" width="63%">
Gets the change unit ID for the change unit that is associated with the exception.


</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitexception-getclockvector">GetClockVector</a>
</td>
<td align="left" width="63%">
Gets the clock vector that is associated with this exception.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/previous-versions/windows/desktop/api/winsync/nf-winsync-ichangeunitexception-getitemid">GetItemId</a>
</td>
<td align="left" width="63%">
Gets the item ID for the item that contains the change unit that is associated with the exception.


</td>
</tr>
</table>

## -see-also

<a href="/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>