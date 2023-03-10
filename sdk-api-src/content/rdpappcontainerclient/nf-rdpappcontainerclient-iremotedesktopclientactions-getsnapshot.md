---
UID: NF:rdpappcontainerclient.IRemoteDesktopClientActions.GetSnapshot
title: IRemoteDesktopClientActions::GetSnapshot (rdpappcontainerclient.h)
description: Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.
helpviewer_keywords: ["GetSnapshot","GetSnapshot method [Remote Desktop Services]","GetSnapshot method [Remote Desktop Services]","IRemoteDesktopClientActions interface","IRemoteDesktopClientActions interface [Remote Desktop Services]","GetSnapshot method","IRemoteDesktopClientActions.GetSnapshot","IRemoteDesktopClientActions::GetSnapshot","rdpappcontainerclient/IRemoteDesktopClientActions::GetSnapshot","termserv.iremotedesktopclientactions_getsnapshot"]
old-location: termserv\iremotedesktopclientactions_getsnapshot.htm
tech.root: TermServ
ms.assetid: c80fe6e3-6ca7-4595-aa0e-c1ed0f6632a5
ms.date: 12/05/2018
ms.keywords: GetSnapshot, GetSnapshot method [Remote Desktop Services], GetSnapshot method [Remote Desktop Services],IRemoteDesktopClientActions interface, IRemoteDesktopClientActions interface [Remote Desktop Services],GetSnapshot method, IRemoteDesktopClientActions.GetSnapshot, IRemoteDesktopClientActions::GetSnapshot, rdpappcontainerclient/IRemoteDesktopClientActions::GetSnapshot, termserv.iremotedesktopclientactions_getsnapshot
req.header: rdpappcontainerclient.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: MsTscAx.dll
req.lib: 
req.dll: MsTscAx.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRemoteDesktopClientActions::GetSnapshot
 - rdpappcontainerclient/IRemoteDesktopClientActions::GetSnapshot
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - MsTscAx.dll
api_name:
 - IRemoteDesktopClientActions.GetSnapshot
---

# IRemoteDesktopClientActions::GetSnapshot


## -description

Causes a snapshot of the Remote Desktop Protocol (RDP) app container client's in-session desktop to be taken.

## -parameters

### -param snapshotEncoding [in]

Specifies the encoding type for the snapshot.

### -param snapshotFormat [in]

Specifies the data format type for the snapshot

### -param snapshotWidth [in]

The width, in pixels, of the snapshot.

### -param snapshotHeight [in]

The height, in pixels, of the snapshot.

### -param snapshotData [out, retval]

On return points to the snapshot.

## -returns

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/rdpappcontainerclient/nn-rdpappcontainerclient-iremotedesktopclientactions">IRemoteDesktopClientActions</a>