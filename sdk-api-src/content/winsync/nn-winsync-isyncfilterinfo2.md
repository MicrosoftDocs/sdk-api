---
UID: NN:winsync.ISyncFilterInfo2
title: ISyncFilterInfo2 (winsync.h)
author: windows-sdk-content
description: Represents additional information about a filter that can be used to control which changes are included in an ISyncChangeBatch object.
old-location: winsync\isyncfilterinfo2.htm
tech.root: winsync
ms.assetid: b1ffc6a7-ca82-4ce6-b7ac-c4c39c59891d
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: ISyncFilterInfo2, ISyncFilterInfo2 interface [Windows Sync], ISyncFilterInfo2 interface [Windows Sync],described, winsync.isyncfilterinfo2, winsync/ISyncFilterInfo2
ms.topic: interface
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
 - ISyncFilterInfo2
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncFilterInfo2 interface


## -description


Represents additional information about a filter that can be used to control which changes are included in an <b>ISyncChangeBatch</b> object.



## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFilterInfo2</b> interface inherits from <a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo</a>. <b>ISyncFilterInfo2</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFilterInfo2</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/cad60957-9d16-4564-b63e-be8e188caecc">GetFlags</a>
</td>
<td align="left" width="63%">
Gets the flags that specify additional information about the filter information object.


</td>
</tr>
</table> 


## -remarks



<b>ISyncFilterInfo2</b> can obtained by calling <b>QueryInterface</b> on an <b>ISyncFilterInfo</b> object or an object derived from <b>ISyncFilterInfo</b>, such as an <b>IChangeUnitListFilterInfo</b> object.




## -see-also




<a href="https://msdn.microsoft.com/fd379fc6-22e5-4165-b4e6-480bc65cccb3">IChangeUnitListFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/89a6d1c4-691d-4356-9ef5-1364b5a7507d">ISyncFilterInfo Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

