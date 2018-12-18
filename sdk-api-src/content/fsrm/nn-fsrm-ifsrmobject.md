---
UID: NN:fsrm.IFsrmObject
title: IFsrmObject
author: windows-sdk-content
description: Base class for all FSRM objects.
old-location: fsrm\ifsrmobject.htm
tech.root: fsrm
ms.assetid: bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IFsrmObject, IFsrmObject interface [File Server Resource Manager], IFsrmObject interface [File Server Resource Manager],described, fs.ifsrmobject, fsrm.ifsrmobject, fsrm/IFsrmObject
ms.topic: interface
req.header: fsrm.h
req.include-header: FsrmPipeline.h, FsrmQuota.h, FsrmReports.h, FsrmScreen.h
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008
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
req.dll: SrmSvc.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - SrmSvc.dll
api_name:
 - IFsrmObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFsrmObject interface


## -description


Base class for all FSRM objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmObject</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms221608(v=VS.85).aspx">IDispatch</a> interface. <b>IFsrmObject</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
<li><a href="https://docs.microsoft.com/">Properties</a></li>
</ul>

## -members

The <b>IFsrmObject</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/81c9b1db-7756-47b2-98e6-8e819d93cd0f">Commit</a>
</td>
<td align="left" width="63%">
Saves the object in the server's list of objects.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/ce8a17fe-377b-4a0e-9a95-7dc25a1411ce">Delete</a>
</td>
<td align="left" width="63%">
Removes the object from the server's list of objects.

</td>
</tr>
</table> 
<h3><a id="properties"></a>Properties</h3>The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmObject</b> interface has these properties.
<table class="members" id="memberListProperties">
<tr>
<th align="left" width="27%">Property</th>
<th align="left" width="10%">Access type</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/8e039e44-17f0-47e7-935b-404af43685bf">Description</a>


</td>
<td align="left" width="10%">
Read/write

</td>
<td align="left" width="63%">
Retrieves or sets the description of the object.

</td>
</tr>
<tr data="declared;">
<td align="left" width="27%" xml:space="preserve">

<a href="https://msdn.microsoft.com/40134594-39e1-416c-9afd-056355bcb0b5">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the object.

</td>
</tr>
</table> 

