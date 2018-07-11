---
UID: NF:syncmgr.ISyncMgrSyncItem.Enable
title: ISyncMgrSyncItem::Enable
author: windows-sdk-content
description: Enables or disables the sync item.
old-location: shell\ISyncMgrSyncItem_Enable.htm
old-project: shell
ms.assetid: 7d73508e-4381-47fe-98ba-ab3ef665cd3e
ms.author: windowssdkdev
ms.date: 06/27/2018
ms.keywords: Enable, Enable method [Windows Shell], Enable method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],Enable method, ISyncMgrSyncItem.Enable, ISyncMgrSyncItem::Enable, _shell_ISyncMgrSyncItem_Enable, shell.ISyncMgrSyncItem_Enable, syncmgr/ISyncMgrSyncItem::Enable
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
 - ISyncMgrSyncItem.Enable
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItem::Enable


## -description


Enables or disables the sync item.


## -parameters




### -param fEnable [in]

Type: <b>BOOL</b>

<b>TRUE</b> to enable; <b>FALSE</b> to disable.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Sync Center calls this method in the following scenarios.
            
                

<ul>
<li>When the user selects the item in the handler's folder and launches its <b>Enable</b> task, but only if the item has not set the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_IPM_PREVENT_ENABLE</a> flag. If the handler supports the <a href="https://msdn.microsoft.com/54336c43-348b-4767-94e4-fe7dc47c0876">SYNCMGR_OBJECTID_QueryBeforeEnable</a> object, this method is only called if the UI operation was successful.</li>
<li>When the user selects the item in the handler's folder and launches its <b>Disable</b> task, but only if the item has not set the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_IPM_PREVENT_DISABLE</a> flag. If the handler supports the <a href="https://msdn.microsoft.com/91441b28-a2d8-4114-86dd-9a3e826deef4">SYNCMGR_OBJECTID_QueryBeforeDisable</a> object, this method is only called if the UI operation was successful.</li>
</ul>
If the handler does not need to perform any actions when it is activated, it can return either S_OK or E_NOTIMPL as shown in the example below.


#### Examples




        	The following example shows a simple implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::Enable(__in BOOL fEnable)
{
    return E_NOTIMPL;
}
</pre>
</td>
</tr>
</table></span></div>


