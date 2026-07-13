---
UID: NF:shobjidl_core.IShellLinkW.SetDescription
title: IShellLinkW::SetDescription (shobjidl_core.h)
description: Sets the description for a Shell link object. The description can be any application-defined string. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetDescription method","IShellLink::SetDescription","IShellLinkA interface [Windows Shell]","SetDescription method","IShellLinkA::SetDescription","IShellLinkW interface [Windows Shell]","SetDescription method","IShellLinkW.SetDescription","IShellLinkW::SetDescription","SetDescription","SetDescription method [Windows Shell]","SetDescription method [Windows Shell]","IShellLink interface","SetDescription method [Windows Shell]","IShellLinkA interface","SetDescription method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetDescription","shell.IShellLink_SetDescription","shobjidl_core/IShellLink::SetDescription","shobjidl_core/IShellLinkA::SetDescription","shobjidl_core/IShellLinkW::SetDescription"]
old-location: shell\IShellLink_SetDescription.htm
tech.root: shell
ms.assetid: 4bec482e-04e6-4cde-ab8e-23c5a1463bdf
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetDescription method, IShellLink::SetDescription, IShellLinkA interface [Windows Shell],SetDescription method, IShellLinkA::SetDescription, IShellLinkW interface [Windows Shell],SetDescription method, IShellLinkW.SetDescription, IShellLinkW::SetDescription, SetDescription, SetDescription method [Windows Shell], SetDescription method [Windows Shell],IShellLink interface, SetDescription method [Windows Shell],IShellLinkA interface, SetDescription method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetDescription, shell.IShellLink_SetDescription, shobjidl_core/IShellLink::SetDescription, shobjidl_core/IShellLinkA::SetDescription, shobjidl_core/IShellLinkW::SetDescription
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
req.dll: Shell32.dll (version 4.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellLinkW::SetDescription
 - shobjidl_core/IShellLinkW::SetDescription
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shell32.dll
api_name:
 - IShellLink.SetDescription
 - IShellLinkA.SetDescription
 - IShellLinkW.SetDescription
---

# IShellLinkW::SetDescription


## -description

Sets the description for a Shell link object. The description can be any application-defined string.

## -parameters

### -param pszName

Type: <b>LPCTSTR</b>

A pointer to a buffer containing the new description string.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For Windows 2000 or later, the string specified by <i>pszName</i> must be no larger than INFOTIPSIZE. For systems prior to Windows 2000, the size of the string is limited by MAX_PATH.

