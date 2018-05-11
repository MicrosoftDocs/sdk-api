---
UID: NF:syncmgr.ISyncMgrSyncItem.GetItemID
title: ISyncMgrSyncItem::GetItemID
author: windows-driver-content
description: Gets the unique ID of a sync item.
old-location: shell\ISyncMgrSyncItem_GetItemID.htm
old-project: shell
ms.assetid: 2add1902-1258-49ed-ad44-35d28d0776c1
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: GetItemID, GetItemID method [Windows Shell], GetItemID method [Windows Shell],ISyncMgrSyncItem interface, ISyncMgrSyncItem interface [Windows Shell],GetItemID method, ISyncMgrSyncItem.GetItemID, ISyncMgrSyncItem::GetItemID, _shell_ISyncMgrSyncItem_GetItemID, shell.ISyncMgrSyncItem_GetItemID, syncmgr/ISyncMgrSyncItem::GetItemID
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
-	ISyncMgrSyncItem.GetItemID
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSyncItem::GetItemID


## -description


Gets the unique ID of a sync item.


## -parameters




### -param ppszItemID [out]

Type: <b>LPWSTR*</b>

When this method returns, contains a pointer to a buffer containing the item's ID. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The ID retrieved by this method cannot change. Typically, the ID is in the form of a GUID string. However, this is not a requirement. The ID can be any string that is unique in the context of the handler.

If <b>GetItemID</b> fails or an empty string is returned in <i>ppszItemID</i>, the sync item is not shown in the handler's folder and Sync Center will not attempt to synchronize it.

The ID retrieved by this method is available in the folder UI as the System.Sync.ItemID (PKEY_Sync_HandlerID) property.

The item is responsible for allocating the string buffer pointed to by <i>ppszComment</i> through <a href="https://msdn.microsoft.com/c4cb588d-9482-4f90-a92e-75b604540d5c">CoTaskMemAlloc</a>. Sync Center deallocates the string buffer through <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a>.

In older Sync Manager implementations, this data was retrieved through the <a href="https://msdn.microsoft.com/84fa1d81-d1b9-44d7-be97-14511ef95528">SYNCMGRITEM</a> structure.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceSyncItem::GetItemID(__out LPWSTR *ppszItemID)
{
    HRESULT hr = S_OK;
    *ppszName = NULL;

    // Generate the string version of the ID.
    if (_pszItemID == NULL)
    {
        LPOLESTR pszItemID = NULL;
        hr = StringFromCLSID(_guidItemID, &amp;_pszItemID);
    }

    if (SUCCEEDED(hr))
    {
        // Duplicate the item ID string for the caller.
        hr = SHCoAllocString(_pszItemID, ppszItemID);
    } 

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


