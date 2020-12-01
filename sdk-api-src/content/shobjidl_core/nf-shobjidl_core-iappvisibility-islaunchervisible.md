---
UID: NF:shobjidl_core.IAppVisibility.IsLauncherVisible
title: IAppVisibility::IsLauncherVisible (shobjidl_core.h)
description: Gets a value that indicates whether the Start screen is displayed.
helpviewer_keywords: ["IAppVisibility interface [Windows Shell]","IsLauncherVisible method","IAppVisibility.IsLauncherVisible","IAppVisibility::IsLauncherVisible","IsLauncherVisible","IsLauncherVisible method [Windows Shell]","IsLauncherVisible method [Windows Shell]","IAppVisibility interface","shell.IAppVisibility_IsLauncherVisible","shobjidl_core/IAppVisibility::IsLauncherVisible"]
old-location: shell\IAppVisibility_IsLauncherVisible.htm
tech.root: shell
ms.assetid: 8D7BBAEC-A745-4707-861E-74CC331ED356
ms.date: 12/05/2018
ms.keywords: IAppVisibility interface [Windows Shell],IsLauncherVisible method, IAppVisibility.IsLauncherVisible, IAppVisibility::IsLauncherVisible, IsLauncherVisible, IsLauncherVisible method [Windows Shell], IsLauncherVisible method [Windows Shell],IAppVisibility interface, shell.IAppVisibility_IsLauncherVisible, shobjidl_core/IAppVisibility::IsLauncherVisible
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8
req.target-min-winversvr: Windows Server 2012
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAppVisibility::IsLauncherVisible
 - shobjidl_core/IAppVisibility::IsLauncherVisible
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IAppVisibility.IsLauncherVisible
---

# IAppVisibility::IsLauncherVisible


## -description

Gets a value that indicates whether the Start screen is displayed.

## -parameters

### -param pfVisible [out]

<b>TRUE</b> if the Start screen is displayed; otherwise, <b>FALSE.</b>

## -returns

This method can return one of these values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_INVALIDARG</b></dt>
</dl>
</td>
<td width="60%">
<i>pfVisible</i> is <b>NULL</b>.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iappvisibility">IAppVisibility</a>