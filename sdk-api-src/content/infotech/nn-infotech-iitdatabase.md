---
UID: NN:infotech.IITDatabase
title: IITDatabase (infotech.h)
description: Use this interface for opening and closing the database object, and for instantiating objects stored in the database.
helpviewer_keywords: ["IITDatabase","IITDatabase interface [HTML Help Workshop]","IITDatabase interface [HTML Help Workshop]","described","htmlhelp.iitdatabase","infotech/IITDatabase","refIITDatabaseInterface"]
old-location: htmlhelp\iitdatabase.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabaseinterface.htm
ms.date: 12/05/2018
ms.keywords: IITDatabase, IITDatabase interface [HTML Help Workshop], IITDatabase interface [HTML Help Workshop],described, htmlhelp.iitdatabase, infotech/IITDatabase, refIITDatabaseInterface
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IITDatabase
 - infotech/IITDatabase
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Infotech.h
api_name:
 - IITDatabase
---

# IITDatabase interface


## -description

Use this interface for opening and closing the database object, and for instantiating objects stored in the database.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITDatabase</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IITDatabase</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IITDatabase</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitdatabase-close">Close</a>
</td>
<td align="left" width="63%">
Closes a database.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitdatabase-createobject">CreateObject</a>
</td>
<td align="left" width="63%">
Creates an unnamed object you can reference in the future through the *<i>pdwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitdatabase-getobject">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a specified <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>-based interface on the object identified by the <i>dwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/infotech/nf-infotech-iitdatabase-open">Open</a>
</td>
<td align="left" width="63%">
Opens a database.



</td>
</tr>
</table>

