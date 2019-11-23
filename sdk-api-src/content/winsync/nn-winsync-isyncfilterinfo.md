---
UID: NN:winsync.ISyncFilterInfo
title: ISyncFilterInfo (winsync.h)

description: Represents information about a filter that is used to control the data that is included in an ISyncChangeBatch object.
old-location: winsync\isyncfilterinfo.htm
tech.root: winsync
ms.assetid: 89a6d1c4-691d-4356-9ef5-1364b5a7507d

ms.date: 12/05/2018
ms.keywords: ISyncFilterInfo, ISyncFilterInfo interface [Windows Sync], ISyncFilterInfo interface [Windows Sync],described, winsync.isyncfilterinfo, winsync/ISyncFilterInfo
ms.topic: interface
f1_keywords: 
 - "winsync/ISyncFilterInfo"
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
 - ISyncFilterInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncFilterInfo interface


## -description


Represents information about a filter that is used to control the data that is included in an <b>ISyncChangeBatch</b> object.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncFilterInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncFilterInfo</b> also has these types of members:
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
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nf-winsync-isyncfilterinfo-serialize">Serialize</a>
</td>
<td align="left" width="63%">
Serializes the filter data to an array of bytes.


</td>
</tr>
</table> 


## -remarks



If a provider filters the contents of a change batch that it creates, it must create a filtered <b>ISyncChangeBatch</b> object.  The filtered change batch object contains an <b>ISyncFilterInfo</b> object that describes how the contents of the change batch were filtered.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/winsync/nn-winsync-isyncchangebatch">ISyncChangeBatch Interface</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/winsync/windows-sync-interfaces">Windows Sync Interfaces</a>
 

 

