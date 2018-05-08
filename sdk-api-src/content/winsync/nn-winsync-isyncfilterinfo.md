---
UID: NN:winsync.ISyncFilterInfo
title: ISyncFilterInfo
author: windows-driver-content
description: Represents information about a filter that is used to control the data that is included in an ISyncChangeBatch object.
old-location: winsync\isyncfilterinfo.htm
old-project: winsync
ms.assetid: 89a6d1c4-691d-4356-9ef5-1364b5a7507d
ms.author: windowsdriverdev
ms.date: 3/14/2018
ms.keywords: ISyncFilterInfo, ISyncFilterInfo interface [Windows Sync], ISyncFilterInfo interface [Windows Sync],described, winsync.isyncfilterinfo, winsync/ISyncFilterInfo
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.typenames: KNOWLEDGE_COOKIE_COMPARISON_RESULT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	winsync.h
api_name:
-	ISyncFilterInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# ISyncFilterInfo interface


## -description


Represents information about a filter that is used to control the data that is included in an <b>ISyncChangeBatch</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFilterInfo</b> interface inherits from the <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> interface. <b>ISyncFilterInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncFilterInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://msdn.microsoft.com/bd3e9fec-9fa2-4216-9a05-1f121bd3dbef">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the filter data to an array of bytes.


</td>
</tr>
</table> 


## -remarks



If a provider filters the contents of a change batch that it creates, it must create a filtered <b>ISyncChangeBatch</b> object.  The filtered change batch object contains an <b>ISyncFilterInfo</b> object that describes how the contents of the change batch were filtered.




## -see-also




<a href="https://msdn.microsoft.com/3bfd5cf2-ca73-490e-84a7-506c198b3d7c">ISyncChangeBatch Interface</a>



<a href="https://msdn.microsoft.com/2c185fe2-1bbe-4409-aea0-6e138430b304">Windows Sync Interfaces</a>
 

 

