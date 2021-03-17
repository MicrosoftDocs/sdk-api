---
UID: NF:mobsync.ISyncMgrSynchronize.GetHandlerInfo
title: ISyncMgrSynchronize::GetHandlerInfo (mobsync.h)
description: Obtains handler information.
helpviewer_keywords: ["GetHandlerInfo","GetHandlerInfo method [Windows Shell]","GetHandlerInfo method [Windows Shell]","ISyncMgrSynchronize interface","ISyncMgrSynchronize interface [Windows Shell]","GetHandlerInfo method","ISyncMgrSynchronize.GetHandlerInfo","ISyncMgrSynchronize::GetHandlerInfo","mobsync/ISyncMgrSynchronize::GetHandlerInfo","shell.syncmgr_isyncmgrsynchronize_gethandlerinfo","syncmgr.isyncmgrsynchronize_gethandlerinfo"]
old-location: shell\syncmgr_isyncmgrsynchronize_gethandlerinfo.htm
tech.root: shell
ms.assetid: bae3ead8-632c-45bf-a24e-bf07922039bd
ms.date: 12/05/2018
ms.keywords: GetHandlerInfo, GetHandlerInfo method [Windows Shell], GetHandlerInfo method [Windows Shell],ISyncMgrSynchronize interface, ISyncMgrSynchronize interface [Windows Shell],GetHandlerInfo method, ISyncMgrSynchronize.GetHandlerInfo, ISyncMgrSynchronize::GetHandlerInfo, mobsync/ISyncMgrSynchronize::GetHandlerInfo, shell.syncmgr_isyncmgrsynchronize_gethandlerinfo, syncmgr.isyncmgrsynchronize_gethandlerinfo
req.header: mobsync.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Mobsync.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ISyncMgrSynchronize::GetHandlerInfo
 - mobsync/ISyncMgrSynchronize::GetHandlerInfo
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mobsync.dll
api_name:
 - ISyncMgrSynchronize.GetHandlerInfo
---

# ISyncMgrSynchronize::GetHandlerInfo


## -description

Obtains handler information.

## -parameters

### -param ppSyncMgrHandlerInfo [out]

Type: <b><a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a>**</b>

A pointer to a <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a> structure.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following:

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Handler information is returned successfully.

</td>
</tr>
</table>

## -remarks

The handler should use the <a href="/windows/desktop/api/combaseapi/nf-combaseapi-cotaskmemalloc">CoTaskMemAlloc</a> function to allocate memory.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgrhandlerinfo">SYNCMGRHANDLERINFO</a>