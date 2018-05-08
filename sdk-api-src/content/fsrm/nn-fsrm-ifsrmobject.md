---
UID: NN:fsrm.IFsrmObject
title: IFsrmObject
author: windows-driver-content
description: Base class for all FSRM objects.
old-location: fsrm\ifsrmobject.htm
old-project: Fsrm
ms.assetid: bb08ea40-6f0e-4ad5-ad57-78f17bbbd4b7
ms.author: windowsdriverdev
ms.date: 4/18/2018
ms.keywords: IFsrmObject, IFsrmObject interface [File Server Resource Manager], IFsrmObject interface [File Server Resource Manager],described, fs.ifsrmobject, fsrm.ifsrmobject, fsrm/IFsrmObject
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: FILTERED_DATA_SOURCES
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	SrmSvc.dll
api_name:
-	IFsrmObject
product: Windows
targetos: Windows
req.lib: 
req.dll: SrmSvc.dll
req.irql: 
req.product: Internet Explorer 5
---

# IFsrmObject interface


## -description


Base class for all FSRM objects.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IFsrmObject</b> interface inherits from the <a href="ebbff4bc-36b2-4861-9efa-ffa45e013eb5">IDispatch</a> interface. <b>IFsrmObject</b> also has these types of members:
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
<a href="https://msdn.microsoft.com/library/windows/hardware/hh439717">Commit</a>
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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn915161">Description</a>


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

<a href="https://msdn.microsoft.com/library/windows/hardware/dn895599">Id</a>


</td>
<td align="left" width="10%">
Read-only

</td>
<td align="left" width="63%">
Retrieves the identifier of the object.

</td>
</tr>
</table> 

