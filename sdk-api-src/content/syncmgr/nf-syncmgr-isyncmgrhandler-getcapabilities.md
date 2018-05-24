---
UID: NF:syncmgr.ISyncMgrHandler.GetCapabilities
title: ISyncMgrHandler::GetCapabilities
author: windows-driver-content
description: Gets a set of flags describing the handler's defined capabilities.
old-location: shell\ISyncMgrHandler_GetCapabilities.htm
old-project: shell
ms.assetid: 3eb43984-f284-4df9-934b-1dd2f0e62e26
ms.author: windowsdriverdev
ms.date: 5/22/2018
ms.keywords: GetCapabilities, GetCapabilities method [Windows Shell], GetCapabilities method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetCapabilities method, ISyncMgrHandler.GetCapabilities, ISyncMgrHandler::GetCapabilities, _shell_ISyncMgrHandler_GetCapabilities, shell.ISyncMgrHandler_GetCapabilities, syncmgr/ISyncMgrHandler::GetCapabilities
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
-	ISyncMgrHandler.GetCapabilities
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandler::GetCapabilities


## -description


Gets a set of flags describing the handler's defined capabilities.


## -parameters




### -param pmCapabilities [out]

Type: <b><a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HANDLER_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HANDLER_CAPABILITIES</a> enumeration that defines the capabilities of the handler. Compare against <a href="https://msdn.microsoft.com/99b0bebf-8131-49d0-bc9d-18fdf41c1371">SYNCMGR_HCM_VALID_MASK</a> to verify a valid value.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method is called by Sync Center in response to a call to <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> or <a href="https://msdn.microsoft.com/752f197e-0dad-4b3d-9f70-352f5f50e9ee">UpdateHandlerCollection</a>.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetCapabilities(
                             __out SYNCMGR_HANDLER_CAPABILITIES *pmCapabilities)
{
    *pmCapabilities = SYNCMGR_HCM_EVENT_STORE
                    | SYNCMGR_HCM_QUERY_BEFORE_ACTIVATE;
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>


