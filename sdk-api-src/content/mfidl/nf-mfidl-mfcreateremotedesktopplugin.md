---
UID: NF:mfidl.MFCreateRemoteDesktopPlugin
title: MFCreateRemoteDesktopPlugin function (mfidl.h)
description: Creates the remote desktop plug-in object. Use this object if the application is running in a Terminal Services client session.
helpviewer_keywords: ["MFCreateRemoteDesktopPlugin","MFCreateRemoteDesktopPlugin function [Media Foundation]","c986c80b-b583-47be-91e7-5881db0018c2","mf.mfcreateremotedesktopplugin","mfidl/MFCreateRemoteDesktopPlugin"]
old-location: mf\mfcreateremotedesktopplugin.htm
tech.root: mf
ms.assetid: c986c80b-b583-47be-91e7-5881db0018c2
ms.date: 12/05/2018
ms.keywords: MFCreateRemoteDesktopPlugin, MFCreateRemoteDesktopPlugin function [Media Foundation], c986c80b-b583-47be-91e7-5881db0018c2, mf.mfcreateremotedesktopplugin, mfidl/MFCreateRemoteDesktopPlugin
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
req.lib: Mf.lib
req.dll: Mf.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - MFCreateRemoteDesktopPlugin
 - mfidl/MFCreateRemoteDesktopPlugin
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - mf.dll
api_name:
 - MFCreateRemoteDesktopPlugin
---

# MFCreateRemoteDesktopPlugin function


## -description

Creates the remote desktop plug-in object. Use this object if the application is running in a Terminal Services client session.

## -parameters

### -param ppPlugin

Receives a pointer to the <a href="/windows/desktop/api/mfidl/nn-mfidl-imfremotedesktopplugin">IMFRemoteDesktopPlugin</a> interface of the plug-in object. The caller must release the interface.

## -returns

The function returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.
          

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
The function succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_ACCESSDENIED</b></dt>
</dl>
</td>
<td width="60%">
Remote desktop connections are not allowed by the current session policy.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/medfound/media-foundation-functions">Media Foundation Functions</a>