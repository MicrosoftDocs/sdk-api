---
UID: NF:syncmgr.ISyncMgrSyncItem.GetItemInfo
title: ISyncMgrSyncItem::GetItemInfo
author: windows-driver-content
description: Gets the properties of a sync item.
old-location: shell\ISyncMgrSyncItem_GetItemInfo.htm
old-project: shell
ms.assetid: b6257d66-36c8-41d6-88f0-99417755582b
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetItemInfo, GetItemInfo method [Windows Shell], GetItemInfo method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetItemInfo method, ISyncMgrSyncItem.GetItemInfo, ISyncMgrSyncItem::GetItemInfo, _shell_ISyncMgrSyncItem_GetItemInfo, shell.ISyncMgrSyncItem_GetItemInfo, syncmgr/ISyncMgrSyncItem::GetItemInfo
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Syncmgr.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Syncmgr.h
api_name:
-	ISyncMgrSyncItem.GetItemInfo
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItem::GetItemInfo


## -description


Gets the properties of a sync item.


## -parameters




### -param ppItemInfo [out]

Type: <b><a href="https://msdn.microsoft.com/b98d216e-f23f-45f3-b42d-e5aa2e540265">ISyncMgrSyncItemInfo</a>*</b>

When this method returns, contains the address of a pointer to an instance of the <a href="https://msdn.microsoft.com/b98d216e-f23f-45f3-b42d-e5aa2e540265">ISyncMgrSyncItemInfo</a> interface, representing the item.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If <b>GetItemInfo</b> fails, the sync item is still shown in the handler's folder and Sync Center continues to synchronize it, but default values are used for all properties.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetItemInfo(
                              __out ISyncMgrSyncItemInfo **ppItemInfo)
{
    *ppItemInfo = NULL;
    
    HRESULT hr = QueryInterface(IID_ISyncMgrSyncItemInfo, (void**)ppItemInfo);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


