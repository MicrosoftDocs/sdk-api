---
UID: NN:cscobj.IOfflineFilesItemContainer
title: IOfflineFilesItemContainer
author: windows-sdk-content
description: Used to access item enumeration functionality in the Offline Files cache.
old-location: of\iofflinefilesitemcontainer.htm
tech.root: offlinefiles
ms.assetid: 328ad076-cafd-461e-8085-7fca65063fa0
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: IOfflineFilesItemContainer, IOfflineFilesItemContainer interface [Offline Files], IOfflineFilesItemContainer interface [Offline Files],described, cscobj/IOfflineFilesItemContainer, of.iofflinefilesitemcontainer
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: interface
req.header: cscobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
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
req.dll: CscSvc.dll; CscObj.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - CscSvc.dll
 - CscObj.dll
api_name:
 - IOfflineFilesItemContainer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IOfflineFilesItemContainer interface


## -description


Used to access item enumeration functionality in the Offline Files cache.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IOfflineFilesItemContainer</b> interface inherits from the <a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a> interface. <b>IOfflineFilesItemContainer</b> also has these types of members:
<ul>
<li><a href="https://msdn.microsoft.com/en-us/library/ms684591(v=VS.85).aspx">Methods</a></li>
</ul>

## -members

The <b>IOfflineFilesItemContainer</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530574(v=VS.85).aspx">EnumItems</a>
</td>
<td align="left" width="63%">
Returns an enumerator of child items for the cache item implementing this method.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/en-us/library/Bb530575(v=VS.85).aspx">EnumItemsEx</a>
</td>
<td align="left" width="63%">
Returns an enumerator of child items for the cache item implementing this method.

</td>
</tr>
</table> 


## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb530659(v=VS.85).aspx">Offline Files API Interfaces</a>
 

 

