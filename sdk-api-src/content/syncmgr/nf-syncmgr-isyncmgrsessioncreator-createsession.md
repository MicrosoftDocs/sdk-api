---
UID: NF:syncmgr.ISyncMgrSessionCreator.CreateSession
title: ISyncMgrSessionCreator::CreateSession method
author: windows-driver-content
description: Notifies Sync Center that synchronization of the specified items has begun.
old-location: shell\ISyncMgrSessionCreator_CreateSession.htm
old-project: shell
ms.assetid: d1df43b6-406c-4da0-89f0-a17e51101520
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CreateSession method [Windows Shell], CreateSession method [Windows Shell], ISyncMgrSessionCreator interface, CreateSession,ISyncMgrSessionCreator.CreateSession, ISyncMgrSessionCreator, ISyncMgrSessionCreator interface [Windows Shell], CreateSession method, ISyncMgrSessionCreator::CreateSession, _shell_ISyncMgrSessionCreator_CreateSession, shell.ISyncMgrSessionCreator_CreateSession, syncmgr/ISyncMgrSessionCreator::CreateSession
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
-	ISyncMgrSessionCreator.CreateSession
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrSessionCreator::CreateSession method


## -description


Notifies Sync Center that synchronization of the specified items has begun.


## -parameters




### -param pszHandlerID [in]

Type: <b>LPCWSTR</b>

A pointer to a buffer containing the unique ID of the handler. This string is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param ppszItemIDs [in]

Type: <b>LPCWSTR*</b>

The address of a pointer to a buffer containing an array of item IDs, managed by the handler specified in <i>pszHandlerID</i>, to be synchronized. Each ID is of maximum length MAX_SYNCMGR_ID including the terminating <b>null</b> character.


### -param cItems [in]

Type: <b>ULONG</b>

The number of item IDs contained in the buffer referenced in <i>ppszItemIDs</i>.


### -param ppCallback [in]

Type: <b><a href="https://msdn.microsoft.com/4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397">ISyncMgrSyncCallback</a>**</b>

The address of a pointer to an instance of <a href="https://msdn.microsoft.com/4f2b6dc3-3b81-4c0a-b0a2-b48f13fba397">ISyncMgrSyncCallback</a> used to report progress and events. This value can be <b>NULL</b> if no callback is needed.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Both <i>pszHandlerID</i> and <i>ppszItemIDs</i> must be specified.


#### Examples




        	The following example shows the outline of an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::Synchronize(...)
{
    ...
    ISyncMgrSyncCallback *pCallback = NULL;

    hr = pCreator-&gt;CreateSession(_pszHandlerID, ppszItemIDs, cItems, &amp;pCallback);
    if (SUCCEEDED(hr))
    {
        // Perform synchronization.
    }

    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


