---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
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
---

# ISyncMgrSyncItem::GetCapabilities


## -description


Gets a set of flags describing the item's defined capabilities.


## -parameters




### -param pmCapabilities [out]

Type: <b><a href="https://msdn.microsoft.com/55f72e18-fba6-4a59-b553-06c6c7c3ee52">SYNCMGR_ITEM_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://msdn.microsoft.com/55f72e18-fba6-4a59-b553-06c6c7c3ee52">SYNCMGR_ITEM_CAPABILITIES</a> enumeration that defines the capabilities of the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by Sync Center in response to a call to <a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">UpdateItem</a>.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetCapabilities(
                              __out SYNCMGR_ITEM_CAPABILITIES *pmCapabilities)
{
    *pmCapabilities = SYNCMGR_ICM_EVENT_STORE
                    | SYNCMGR_ICM_CAN_DELETE
                    | SYNCMGR_ICM_QUERY_BEFORE_DELETE;
    
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>


