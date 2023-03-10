---
UID: NF:shobjidl_core.ILaunchTargetViewSizePreference.GetTargetViewSizePreference
title: ILaunchTargetViewSizePreference::GetTargetViewSizePreference (shobjidl_core.h)
description: Retrieves the preferred view size of the application being launched.
helpviewer_keywords: ["GetTargetViewSizePreference","GetTargetViewSizePreference method [Windows Shell]","GetTargetViewSizePreference method [Windows Shell]","ILaunchTargetViewSizePreference interface","ILaunchTargetViewSizePreference interface [Windows Shell]","GetTargetViewSizePreference method","ILaunchTargetViewSizePreference.GetTargetViewSizePreference","ILaunchTargetViewSizePreference::GetTargetViewSizePreference","shell.ILaunchTargetViewSizePreference_GetTargetViewSizePreference","shobjidl_core/ILaunchTargetViewSizePreference::GetTargetViewSizePreference"]
old-location: shell\ILaunchTargetViewSizePreference_GetTargetViewSizePreference.htm
tech.root: shell
ms.assetid: 2C852FD1-09FD-45B6-A493-07DEE72BEA4C
ms.date: 12/05/2018
ms.keywords: GetTargetViewSizePreference, GetTargetViewSizePreference method [Windows Shell], GetTargetViewSizePreference method [Windows Shell],ILaunchTargetViewSizePreference interface, ILaunchTargetViewSizePreference interface [Windows Shell],GetTargetViewSizePreference method, ILaunchTargetViewSizePreference.GetTargetViewSizePreference, ILaunchTargetViewSizePreference::GetTargetViewSizePreference, shell.ILaunchTargetViewSizePreference_GetTargetViewSizePreference, shobjidl_core/ILaunchTargetViewSizePreference::GetTargetViewSizePreference
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
 - ILaunchTargetViewSizePreference::GetTargetViewSizePreference
 - shobjidl_core/ILaunchTargetViewSizePreference::GetTargetViewSizePreference
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
 - ILaunchTargetViewSizePreference.GetTargetViewSizePreference
---

# ILaunchTargetViewSizePreference::GetTargetViewSizePreference


## -description

Retrieves the preferred view size of the application being launched.

## -parameters

### -param targetSizeOnLaunch [out]

Type: <b><a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_size_preference">APPLICATION_VIEW_SIZE_PREFERENCE</a>*</b>

Contains the address of a pointer to an <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-application_view_size_preference">APPLICATION_VIEW_SIZE_PREFERENCE</a>  for the target application.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ilaunchtargetviewsizepreference">ILaunchTargetViewSizePreference</a>