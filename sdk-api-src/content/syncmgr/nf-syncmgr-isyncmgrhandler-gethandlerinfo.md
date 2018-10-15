---
UID: NF:syncmgr.ISyncMgrHandler.GetHandlerInfo
title: ISyncMgrHandler::GetHandlerInfo
author: windows-sdk-content
description: Gets properties that describe the handler.
old-location: shell\ISyncMgrHandler_GetHandlerInfo.htm
tech.root: shell
ms.assetid: 078f7cee-fb75-4b8b-8c90-720c26d1f361
ms.author: windowssdkdev
ms.date: 10/10/2018
ms.keywords: GetHandlerInfo, GetHandlerInfo method [Windows Shell], GetHandlerInfo method [Windows Shell],ISyncMgrHandler interface, ISyncMgrHandler interface [Windows Shell],GetHandlerInfo method, ISyncMgrHandler.GetHandlerInfo, ISyncMgrHandler::GetHandlerInfo, _shell_ISyncMgrHandler_GetHandlerInfo, shell.ISyncMgrHandler_GetHandlerInfo, syncmgr/ISyncMgrHandler::GetHandlerInfo
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
req.lib: 
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Syncmgr.h
api_name:
 - ISyncMgrHandler.GetHandlerInfo
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# ISyncMgrHandler::GetHandlerInfo


## -description


Gets properties that describe the handler.


## -parameters




### -param ppHandlerInfo [out]

Type: <b><a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a>**</b>

When this method returns, contains the address of a pointer to an instance of the <a href="https://msdn.microsoft.com/29cded59-d0f3-4678-9601-4931687b48e4">ISyncMgrHandlerInfo</a> interface that provides access to the handler properties.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If this method fails, the handler is still shown in the Sync Center folder and Sync Center continues to invoke it, but default values are used for all properties.

<b>ISyncMgrHandler::GetHandlerInfo</b>, together with <a href="https://msdn.microsoft.com/2d981cf9-6c0a-4bca-b088-06eb1c820fb3">ISyncMgrHandler::GetName</a>, replaces the older <a href="https://msdn.microsoft.com/bae3ead8-632c-45bf-a24e-bf07922039bd">GetHandlerInfo</a>.


#### Examples



The following example shows an implementation of this method.

<div class="code"><span codelanguage="ManagedCPlusPlus"><table>
<tr>
<th>C++</th>
</tr>
<tr>
<td>
<pre>STDMETHODIMP CMyDeviceHandler::GetHandlerInfo(
                             __out ISyncMgrHandlerInfo **ppHandlerInfo)
{
    *ppHandlerInfo = NULL;
    HRESULT hr = QueryInterface(IID_ISyncMgrHandlerInfo, 
                                (void **) ppHandlerInfo);
    return hr;
}
</pre>
</td>
</tr>
</table></span></div>


