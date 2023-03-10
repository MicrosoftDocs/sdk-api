---
UID: NF:mfidl.IMFRemoteDesktopPlugin.UpdateTopology
title: IMFRemoteDesktopPlugin::UpdateTopology (mfidl.h)
description: Modifies a topology for use in a Terminal Services environment. (IMFRemoteDesktopPlugin.UpdateTopology)
helpviewer_keywords: ["799ba0b4-b015-4899-9496-d8c23d033b24","IMFRemoteDesktopPlugin interface [Media Foundation]","UpdateTopology method","IMFRemoteDesktopPlugin.UpdateTopology","IMFRemoteDesktopPlugin::UpdateTopology","UpdateTopology","UpdateTopology method [Media Foundation]","UpdateTopology method [Media Foundation]","IMFRemoteDesktopPlugin interface","mf.imfremotedesktopplugin_updatetopology","mfidl/IMFRemoteDesktopPlugin::UpdateTopology"]
old-location: mf\imfremotedesktopplugin_updatetopology.htm
tech.root: mf
ms.assetid: 799ba0b4-b015-4899-9496-d8c23d033b24
ms.date: 12/05/2018
ms.keywords: 799ba0b4-b015-4899-9496-d8c23d033b24, IMFRemoteDesktopPlugin interface [Media Foundation],UpdateTopology method, IMFRemoteDesktopPlugin.UpdateTopology, IMFRemoteDesktopPlugin::UpdateTopology, UpdateTopology, UpdateTopology method [Media Foundation], UpdateTopology method [Media Foundation],IMFRemoteDesktopPlugin interface, mf.imfremotedesktopplugin_updatetopology, mfidl/IMFRemoteDesktopPlugin::UpdateTopology
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMFRemoteDesktopPlugin::UpdateTopology
 - mfidl/IMFRemoteDesktopPlugin::UpdateTopology
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - mfuuid.lib
 - mfuuid.dll
api_name:
 - IMFRemoteDesktopPlugin.UpdateTopology
---

# IMFRemoteDesktopPlugin::UpdateTopology


## -description

Modifies a topology for use in a Terminal Services environment.

## -parameters

### -param pTopology [in, out]

Pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imftopology">IMFTopology</a> interface of the topology.

## -returns

The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

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
The method succeeded.

</td>
</tr>
</table>

## -remarks

If the application is running in a Terminal Services client session, call this method before calling <a href="/windows/desktop/api/mfidl/nf-mfidl-imfmediasession-settopology">IMFMediaSession::SetTopology</a> on the Media Session.

## -see-also

<a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin">IMFRemoteDesktopPlugin</a>
