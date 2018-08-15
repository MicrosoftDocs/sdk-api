---
UID: NF:wmp.IWMPMediaCollection.setDeleted
title: IWMPMediaCollection::setDeleted
author: windows-sdk-content
description: The setDeleted method moves the specified media item to the deleted items folder.
old-location: wmp\iwmpmediacollection_setdeleted.htm
old-project: WMP
ms.assetid: 4bba1e7a-3c1f-4f69-b4ab-68a9cf3b97d0
ms.author: windowssdkdev
ms.date: 07/30/2018
ms.keywords: IWMPMediaCollection interface [Windows Media Player],setDeleted method, IWMPMediaCollection.setDeleted, IWMPMediaCollection::setDeleted, IWMPMediaCollectionsetDeleted, setDeleted, setDeleted method [Windows Media Player], setDeleted method [Windows Media Player],IWMPMediaCollection interface, wmp.iwmpmediacollection_setdeleted, wmp/IWMPMediaCollection::setDeleted
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: wmp.h
req.include-header: 
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 9 Series or later.
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
tech.root: 
req.typenames: WMPSyncState
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPMediaCollection.setDeleted
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPMediaCollection::setDeleted


## -description



The <b>setDeleted</b> method moves the specified media item to the deleted items folder.




## -parameters




### -param pItem [in]

Pointer to an <b>IWMPMedia</b> interface for the item to be moved.


### -param varfIsDeleted [in]

Specifies whether the item should be moved. This value must always be true.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
</table>
 




## -remarks



This method does not remove files from the user's computer.

Before calling this method, you must have read access to the library. For more information, see <a href="https://msdn.microsoft.com/9f722531-a551-4ca9-be5f-01a291a180b0">Library Access</a>.

<b>Windows Media Player 10 Mobile:</b> This method always returns E_INVALIDARG.




## -see-also




<a href="https://msdn.microsoft.com/2311067c-b731-47d2-880d-73870fee7694">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/bf975a30-dfb1-4994-9095-510a6b997aff">IWMPMediaCollection Interface</a>
 

 

