---
UID: NF:shobjidl_core.IShellLinkW.GetDescription
title: IShellLinkW::GetDescription (shobjidl_core.h)
description: Gets the description string for a Shell link object. (Unicode)
helpviewer_keywords: ["GetDescription","GetDescription method [Windows Shell]","GetDescription method [Windows Shell]","IShellLink interface","GetDescription method [Windows Shell]","IShellLinkA interface","GetDescription method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetDescription method","IShellLink::GetDescription","IShellLinkA interface [Windows Shell]","GetDescription method","IShellLinkA::GetDescription","IShellLinkW interface [Windows Shell]","GetDescription method","IShellLinkW.GetDescription","IShellLinkW::GetDescription","_win32_IShellLink_GetDescription","shell.IShellLink_GetDescription","shobjidl_core/IShellLink::GetDescription","shobjidl_core/IShellLinkA::GetDescription","shobjidl_core/IShellLinkW::GetDescription"]
old-location: shell\IShellLink_GetDescription.htm
tech.root: shell
ms.assetid: 1f00a485-42b5-4f91-88e0-d2ce78273be1
ms.date: 12/05/2018
ms.keywords: GetDescription, GetDescription method [Windows Shell], GetDescription method [Windows Shell],IShellLink interface, GetDescription method [Windows Shell],IShellLinkA interface, GetDescription method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetDescription method, IShellLink::GetDescription, IShellLinkA interface [Windows Shell],GetDescription method, IShellLinkA::GetDescription, IShellLinkW interface [Windows Shell],GetDescription method, IShellLinkW.GetDescription, IShellLinkW::GetDescription, _win32_IShellLink_GetDescription, shell.IShellLink_GetDescription, shobjidl_core/IShellLink::GetDescription, shobjidl_core/IShellLinkA::GetDescription, shobjidl_core/IShellLinkW::GetDescription
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
 - IShellLinkW::GetDescription
 - shobjidl_core/IShellLinkW::GetDescription
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
 - IShellLink.GetDescription
 - IShellLinkA.GetDescription
 - IShellLinkW.GetDescription
---

# IShellLinkW::GetDescription


## -description

Gets the description string for a Shell link object.

## -parameters

### -param pszName

Type: <b>LPTSTR</b>

A pointer to the buffer that receives the description string.

### -param cch

Type: <b>int</b>

The maximum number of characters to copy to the buffer pointed to by the <i>pszName</i> parameter.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For Windows 2000 or later, the string returned to <i>pszName</i> has a maximum length of INFOTIPSIZE. For systems prior to Windows 2000, the size of the string is limited by MAX_PATH.

