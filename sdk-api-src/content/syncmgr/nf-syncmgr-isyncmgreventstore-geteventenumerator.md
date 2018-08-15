---
UID: NF:syncmgr.ISyncMgrEventStore.GetEventEnumerator
title: ISyncMgrEventStore::GetEventEnumerator
author: windows-sdk-content
description: Gets an enumerator for a handler's events.
old-location: shell\ISyncMgrEventStore_GetEventEnumerator.htm
old-project: shell
ms.assetid: 8b634811-cb6d-47b2-b534-1baea23a5297
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEventEnumerator, GetEventEnumerator method [Windows Shell], GetEventEnumerator method [Windows Shell],ISyncMgrEventStore interface, ISyncMgrEventStore interface [Windows Shell],GetEventEnumerator method, ISyncMgrEventStore.GetEventEnumerator, ISyncMgrEventStore::GetEventEnumerator, _shell_ISyncMgrEventStore_GetEventEnumerator, shell.ISyncMgrEventStore_GetEventEnumerator, syncmgr/ISyncMgrEventStore::GetEventEnumerator
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: syncmgr.h
req.include-header: 
req.redist: 
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
 - ISyncMgrEventStore.GetEventEnumerator
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrEventStore::GetEventEnumerator


## -description


Gets an enumerator for a handler's events.


## -parameters




### -param ppenum [out]

Type: <b><a href="https://msdn.microsoft.com/74d0c373-e9b1-4d9c-bdb6-caa743938e32">IEnumSyncMgrEvents</a>**</b>

When this method returns, contains the address of a pointer to an <a href="https://msdn.microsoft.com/74d0c373-e9b1-4d9c-bdb6-caa743938e32">IEnumSyncMgrEvents</a> instance that can be used to access the handler's events.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by Sync Center when the user navigates to the Sync Results folder or clicks the <b>Errors</b> link for a handler.


#### Examples



The following example shows an implementation of <b>ISyncMgrEventStore::GetEventEnumerator</b>.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceEventStore::GetEventEnumerator(
                                __out IEnumSyncMgrEvents **ppenum)
{
    HRESULT hr = CEnumMyDeviceSyncMgrEvents_Create(ppenum);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


