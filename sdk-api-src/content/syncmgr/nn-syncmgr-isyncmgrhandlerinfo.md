---
UID: NN:syncmgr.ISyncMgrHandlerInfo
title: ISyncMgrHandlerInfo (syncmgr.h)
description: Exposes methods that allow a handler to provide property and state information to Sync Center.helpviewer_keywords: ["ISyncMgrHandlerInfo","ISyncMgrHandlerInfo interface [Windows Shell]","ISyncMgrHandlerInfo interface [Windows Shell]","described","_shell_ISyncMgrHandlerInfo","shell.ISyncMgrHandlerInfo","syncmgr/ISyncMgrHandlerInfo"]
old-location: shell\ISyncMgrHandlerInfo.htm
tech.root: shell
ms.assetid: 29cded59-d0f3-4678-9601-4931687b48e4
ms.date: 12/05/2018
ms.keywords: ISyncMgrHandlerInfo, ISyncMgrHandlerInfo interface [Windows Shell], ISyncMgrHandlerInfo interface [Windows Shell],described, _shell_ISyncMgrHandlerInfo, shell.ISyncMgrHandlerInfo, syncmgr/ISyncMgrHandlerInfo
f1_keywords:
- syncmgr/ISyncMgrHandlerInfo
dev_langs:
- c++
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
- ISyncMgrHandlerInfo
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# ISyncMgrHandlerInfo interface


## -description


Exposes methods that allow a handler to provide property and state information to Sync Center.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ISyncMgrHandlerInfo</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ISyncMgrHandlerInfo</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ISyncMgrHandlerInfo</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-getcomment">GetComment</a>
</td>
<td align="left" width="63%">
Gets a string that contains commentary regarding the handler.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-getlastsynctime">GetLastSyncTime</a>
</td>
<td align="left" width="63%">
Gets the date and time when the handler was last synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettype">GetType</a>
</td>
<td align="left" width="63%">
Gets the handler type for Sync Center.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-gettypelabel">GetTypeLabel</a>
</td>
<td align="left" width="63%">
Gets a label for the handler type. This typically provides the model of the device or an equivalent handler-specific identity string.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-isactive">IsActive</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler can be synchronized.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-isconnected">IsConnected</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler—typically some type of external device—is connected.

</td>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nf-syncmgr-isyncmgrhandlerinfo-isenabled">IsEnabled</a>
</td>
<td align="left" width="63%">
Gets a value that indicates whether the handler is enabled.

</td>
</tr>
</table> 


## -remarks



Handlers should always implement this interface, generally on the same object that implements <a href="https://docs.microsoft.com/windows/desktop/api/syncmgr/nn-syncmgr-isyncmgrhandler">ISyncMgrHandler</a>. By implementing <b>ISyncMgrHandlerInfo</b>, the set of properties can be changed without requiring the handler to be recompiled. It also provides type-safe access to the properties.



