---
UID: NF:syncmgr.ISyncMgrSyncItem.GetPolicies
title: ISyncMgrSyncItem::GetPolicies
author: windows-sdk-content
description: Gets a set of flags describing the policies set by the item.
old-location: shell\ISyncMgrSyncItem_GetPolicies.htm
old-project: shell
ms.assetid: 5f4e1a8e-8fa7-48b3-8f20-8b260540ab9c
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: GetPolicies, GetPolicies method [Windows Shell], GetPolicies method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetPolicies method, ISyncMgrSyncItem.GetPolicies, ISyncMgrSyncItem::GetPolicies, _shell_ISyncMgrSyncItem_GetPolicies, shell.ISyncMgrSyncItem_GetPolicies, syncmgr/ISyncMgrSyncItem::GetPolicies
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: SYNCMGR_SYNC_CONTROL_FLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrSyncItem.GetPolicies
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItem::GetPolicies


## -description


Gets a set of flags describing the policies set by the item.


## -parameters




### -param pmPolicies [out]

Type: <b><a href="https://msdn.microsoft.com/d894beca-855c-472f-931a-db5c6f3f891e">SYNCMGR_ITEM_POLICIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://msdn.microsoft.com/d894beca-855c-472f-931a-db5c6f3f891e">SYNCMGR_ITEM_POLICIES</a> enumeration that defines the item's policies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A policy is an action that is typically supported but can be disabled by a group policy.

This method is called by Sync Center in response to a call to <a href="https://msdn.microsoft.com/deb87d2f-74da-450a-a424-505240eadacb">UpdateItem</a>.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetPolicies(
                              __out SYNCMGR_ITEM_POLICIES *pmPolicies)
{
    *pmPolicies = SYNCMGR_IPM_PREVENT_DISABLE 
                | SYNCMGR_IPM_HIDDEN_BY_DEFAULT;
                
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>


