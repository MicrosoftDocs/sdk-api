---
UID: NN:infotech.IITDatabase
title: IITDatabase
author: windows-driver-content
description: Use this interface for opening and closing the database object, and for instantiating objects stored in the database.
old-location: htmlhelp\iitdatabase.htm
old-project: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabaseinterface.htm
ms.author: windowsdriverdev
ms.date: 2/15/2018
ms.keywords: IITDatabase, IITDatabase interface [HTML Help Workshop], IITDatabase interface [HTML Help Workshop], described, htmlhelp.iitdatabase, infotech/IITDatabase, refIITDatabaseInterface
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: POLICY_ELEMENT, *PPOLICY_ELEMENT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Infotech.h
api_name:
-	IITDatabase
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IITDatabase interface


## -description


Use this interface for opening and closing the database object, and for instantiating objects stored in the database.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IITDatabase</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>IITDatabase</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451151">Close</a>
</td>
<td align="left" width="63%">
Closes a database.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/8191ab96-0303-4972-ae9b-8f2f8a23ac1a">CreateObject</a>
</td>
<td align="left" width="63%">
Creates an unnamed object you can reference in the future through the *<i>pdwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/f83a48da-8f11-4af3-9de8-a2eabd1432ec">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a specified <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-based interface on the object identified by the <i>dwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/library/windows/hardware/hh451153">Open</a>
</td>
<td align="left" width="63%">
Opens a database.



</td>
</tr>
</table> 

