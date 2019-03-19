---
UID: NN:infotech.IITDatabase
title: IITDatabase (infotech.h)
author: windows-sdk-content
description: Use this interface for opening and closing the database object, and for instantiating objects stored in the database.
old-location: htmlhelp\iitdatabase.htm
tech.root: htmlhelp
ms.assetid: VS|htmlhelp|~\html\refiitdatabaseinterface.htm
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IITDatabase, IITDatabase interface [HTML Help Workshop], IITDatabase interface [HTML Help Workshop],described, htmlhelp.iitdatabase, infotech/IITDatabase, refIITDatabaseInterface
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
 - IITDatabase
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
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
<a href="https://msdn.microsoft.com/en-us/library/ms670031(v=VS.85).aspx">Close</a>
</td>
<td align="left" width="63%">
Closes a database.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670032(v=VS.85).aspx">CreateObject</a>
</td>
<td align="left" width="63%">
Creates an unnamed object you can reference in the future through the *<i>pdwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670033(v=VS.85).aspx">GetObject</a>
</td>
<td align="left" width="63%">
Retrieves a specified <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>-based interface on the object identified by the <i>dwObjInstance</i> parameter.



</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/ms670035(v=VS.85).aspx">Open</a>
</td>
<td align="left" width="63%">
Opens a database.



</td>
</tr>
</table> 

