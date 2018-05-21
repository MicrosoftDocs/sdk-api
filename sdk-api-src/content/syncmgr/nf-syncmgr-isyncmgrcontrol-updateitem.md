---
UID: NF:syncmgr.ISyncMgrControl.UpdateItem
title: ISyncMgrControl::UpdateItem
author: windows-driver-content
description: Informs Sync Center that properties of a sync item have changed.
old-location: shell\ISyncMgrControl_UpdateItem.htm
old-project: shell
ms.assetid: deb87d2f-74da-450a-a424-505240eadacb
ms.author: windowsdriverdev
ms.date: 5/16/2018
ms.keywords: ISyncMgrControl interface [Windows Shell],UpdateItem method, ISyncMgrControl.UpdateItem, ISyncMgrControl::UpdateItem, UpdateItem, UpdateItem method [Windows Shell], UpdateItem method [Windows Shell],ISyncMgrControl interface, _shell_ISyncMgrControl_UpdateItem, shell.ISyncMgrControl_UpdateItem, syncmgr/ISyncMgrControl::UpdateItem
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
-	ISyncMgrControl.UpdateItem
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrControl::UpdateItem


## -description


Informs Sync Center that properties of a sync item have changed.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler that manages the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param pszItemID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the item. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param nControlFlags [in]

Type: <b><a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a></b>

A value from the <a href="https://msdn.microsoft.com/cfba36ba-8cbd-41ae-91ae-e568546508b9">SYNCMGR_CONTROL_FLAGS</a> enumeration specifying whether the update should be performed synchronously or asynchronously.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If SYNCMGR_CF_WAIT is set in the <i>nControlFlags</i> parameter, <b>UpdateItem</b> does not return until Sync Center has loaded the specified handler and reloaded all handler and item information. If the handler is provided by a handler collection, the handler collection is also loaded to reload the handler.


#### Examples




        	The following example shows the usage of <b>ISyncMgrControl::UpdateItem</b> by a handler's procedure.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>void CMyDeviceHandler::MiscProc(...)
{
    ...

    // Get the Sync Center control object.
    ISyncMgrControl *pControl = NULL;
    
    hr = CoCreateInstance(CLSID_SyncMgrControl, 
                          CLSCTX_SERVER, 
                          IID_PPV_ARGS(&amp;pControl));
    if (SUCCEEDED(hr))
    {
        // Tell Sync Center that properties of the item have changed.
        hr = pControl-&gt;UpdateItem(s_szMySyncHandlerID,
                                  s_szMySyncHandlerMusicContentID,
                                  SYNCMGR_CF_WAIT);
        pControl-&gt;Release();
    }

    ...

}
</pre>
</td>
</tr>
</table></span></div>


