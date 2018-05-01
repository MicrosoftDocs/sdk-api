---
UID: NF:syncmgr.ISyncMgrHandler.GetPolicies
title: ISyncMgrHandler::GetPolicies method
author: windows-driver-content
description: Gets a set of flags describing the policies set by the handler.
old-location: shell\ISyncMgrHandler_GetPolicies.htm
old-project: shell
ms.assetid: ff30441a-43bb-4f30-af04-4d2056b8dfb0
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: GetPolicies method [Windows Shell], GetPolicies method [Windows Shell], ISyncMgrHandler interface, GetPolicies,ISyncMgrHandler.GetPolicies, ISyncMgrHandler, ISyncMgrHandler interface [Windows Shell], GetPolicies method, ISyncMgrHandler::GetPolicies, _shell_ISyncMgrHandler_GetPolicies, shell.ISyncMgrHandler_GetPolicies, syncmgr/ISyncMgrHandler::GetPolicies
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
-	ISyncMgrHandler.GetPolicies
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows XP with SP1 and later
---

# ISyncMgrHandler::GetPolicies method


## -description


Gets a set of flags describing the policies set by the handler.


## -parameters




### -param pmPolicies [out]

Type: <b><a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_HANDLER_POLICIES</a>*</b>

When this method returns, contains a pointer to a bitwise combination of values from the <a href="https://msdn.microsoft.com/2baf39ea-2b28-4d38-8635-8f5efca54702">SYNCMGR_HANDLER_POLICIES</a> enumeration that define the handler's policies.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



A policy is an action that is usually supported but can be disabled by a group policy.

This method is called by Sync Center in response to a call to <a href="https://msdn.microsoft.com/d961aef7-c559-4caa-894e-e86836b142c0">UpdateHandler</a> or <a href="https://msdn.microsoft.com/752f197e-0dad-4b3d-9f70-352f5f50e9ee">UpdateHandlerCollection</a>.


#### Examples




        	The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetPolicies(
                             __out SYNCMGR_HANDLER_POLICIES *pmPolicies)
{
    *pmPolicies = SYNCMGR_HPM_NONE;
    return S_OK;
}
</pre>
</td>
</tr>
</table></span></div>


