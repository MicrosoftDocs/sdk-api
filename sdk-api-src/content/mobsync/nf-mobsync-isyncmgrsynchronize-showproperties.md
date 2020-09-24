---
UID: NF:mobsync.ISyncMgrSynchronize.ShowProperties
title: ISyncMgrSynchronize::ShowProperties (mobsync.h)
description: Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the Properties button.
helpviewer_keywords: ["ISyncMgrSynchronize interface [Windows Shell]","ShowProperties method","ISyncMgrSynchronize.ShowProperties","ISyncMgrSynchronize::ShowProperties","ShowProperties","ShowProperties method [Windows Shell]","ShowProperties method [Windows Shell]","ISyncMgrSynchronize interface","mobsync/ISyncMgrSynchronize::ShowProperties","shell.syncmgr_isyncmgrsynchronize_showproperties","syncmgr.isyncmgrsynchronize_showproperties"]
old-location: shell\syncmgr_isyncmgrsynchronize_showproperties.htm
tech.root: shell
ms.assetid: 5587cc8a-b359-483e-98ba-82f1bbe058d8
ms.date: 12/05/2018
ms.keywords: ISyncMgrSynchronize interface [Windows Shell],ShowProperties method, ISyncMgrSynchronize.ShowProperties, ISyncMgrSynchronize::ShowProperties, ShowProperties, ShowProperties method [Windows Shell], ShowProperties method [Windows Shell],ISyncMgrSynchronize interface, mobsync/ISyncMgrSynchronize::ShowProperties, shell.syncmgr_isyncmgrsynchronize_showproperties, syncmgr.isyncmgrsynchronize_showproperties
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
 - ISyncMgrSynchronize::ShowProperties
 - mobsync/ISyncMgrSynchronize::ShowProperties
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
 - ISyncMgrSynchronize.ShowProperties
---

# ISyncMgrSynchronize::ShowProperties


## -description

Called by the synchronization manager when a user selects an item in the choice dialog box, and then clicks the <b>Properties</b> button.

## -parameters

### -param hWndParent [in]

Type: <b>HWND</b>

The parent <b>HWND</b> for any user interface that a registered application displays to set properties. This value can be <b>NULL</b>.

### -param ItemID [in]

Type: <b>REFGUID</b>

The item ID for properties that are requested.

## -returns

Type: <b>HRESULT</b>

This method supports the standard return values E_INVALIDARG, E_UNEXPECTED, and E_OUTOFMEMORY, and the following.

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
The properties dialog for an item is handled successfully.

</td>
</tr>
</table>

## -remarks

If a registered application provides a properties dialog box for an item, it must set the SYNCMGRITEM_HASPROPERTIES bit in the <b>dwFlags</b> member of the <a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a> structure.

If <i>ItemID</i> is GUID_NULL the handler should show the properties dialog for the overall handler.

The appearance of the displayed dialog box should be consistent with a standard property page dialog box.

## -see-also

<a href="/windows/desktop/api/mobsync/nn-mobsync-isyncmgrsynchronize">ISyncMgrSynchronize</a>



<a href="/windows/desktop/api/mobsync/ns-mobsync-syncmgritem">SYNCMGRITEM</a>



<a href="/windows/desktop/api/mobsync/ne-mobsync-syncmgritemflags">SYNCMGRITEMFLAGS</a>