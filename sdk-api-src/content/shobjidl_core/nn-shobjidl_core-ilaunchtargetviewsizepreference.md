---
UID: NN:shobjidl_core.ILaunchTargetViewSizePreference
title: ILaunchTargetViewSizePreference (shobjidl_core.h)
description: Provides a method for retrieving the preferred view size for a new application window.
helpviewer_keywords: ["ILaunchTargetViewSizePreference","ILaunchTargetViewSizePreference interface [Windows Shell]","ILaunchTargetViewSizePreference interface [Windows Shell]","described","shell.ILaunchTargetViewSizePreference","shobjidl_core/ILaunchTargetViewSizePreference"]
old-location: shell\ILaunchTargetViewSizePreference.htm
tech.root: shell
ms.assetid: 3535E9EF-265E-4278-8E0D-60AA8A34C316
ms.date: 12/05/2018
ms.keywords: ILaunchTargetViewSizePreference, ILaunchTargetViewSizePreference interface [Windows Shell], ILaunchTargetViewSizePreference interface [Windows Shell],described, shell.ILaunchTargetViewSizePreference, shobjidl_core/ILaunchTargetViewSizePreference
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8.1 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 R2 [desktop apps only]
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
 - ILaunchTargetViewSizePreference
 - shobjidl_core/ILaunchTargetViewSizePreference
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
 - ILaunchTargetViewSizePreference
---

# ILaunchTargetViewSizePreference interface


## -description

Provides a method for retrieving the preferred view size for a new application window.

## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">ILaunchTargetViewSizePreference</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ILaunchTargetViewSizePreference</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>ILaunchTargetViewSizePreference</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ilaunchtargetviewsizepreference-gettargetviewsizepreference">GetTargetViewSizePreference</a>
</td>
<td align="left" width="63%">
Retrieves the preferred view size of the application being launched.

</td>
</tr>
</table>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchsourceviewsizepreference">ILaunchSourceViewSizePreference</a>



<a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a>