---
UID: NF:shobjidl_core.IShellLinkW.SetArguments
title: IShellLinkW::SetArguments (shobjidl_core.h)
description: Sets the command-line arguments for a Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetArguments method","IShellLink::SetArguments","IShellLinkA interface [Windows Shell]","SetArguments method","IShellLinkA::SetArguments","IShellLinkW interface [Windows Shell]","SetArguments method","IShellLinkW.SetArguments","IShellLinkW::SetArguments","SetArguments","SetArguments method [Windows Shell]","SetArguments method [Windows Shell]","IShellLink interface","SetArguments method [Windows Shell]","IShellLinkA interface","SetArguments method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetArguments","shell.IShellLink_SetArguments","shobjidl_core/IShellLink::SetArguments","shobjidl_core/IShellLinkA::SetArguments","shobjidl_core/IShellLinkW::SetArguments"]
old-location: shell\IShellLink_SetArguments.htm
tech.root: shell
ms.assetid: 5ad5fabd-be12-40bc-a6b3-498bcde7223a
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetArguments method, IShellLink::SetArguments, IShellLinkA interface [Windows Shell],SetArguments method, IShellLinkA::SetArguments, IShellLinkW interface [Windows Shell],SetArguments method, IShellLinkW.SetArguments, IShellLinkW::SetArguments, SetArguments, SetArguments method [Windows Shell], SetArguments method [Windows Shell],IShellLink interface, SetArguments method [Windows Shell],IShellLinkA interface, SetArguments method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetArguments, shell.IShellLink_SetArguments, shobjidl_core/IShellLink::SetArguments, shobjidl_core/IShellLinkA::SetArguments, shobjidl_core/IShellLinkW::SetArguments
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
 - IShellLinkW::SetArguments
 - shobjidl_core/IShellLinkW::SetArguments
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
 - IShellLink.SetArguments
 - IShellLinkA.SetArguments
 - IShellLinkW.SetArguments
---

# IShellLinkW::SetArguments


## -description

Sets the command-line arguments for a Shell link object.

## -parameters

### -param pszArgs [in]

Type: <b>LPCTSTR</b>

A pointer to a buffer that contains the new command-line arguments. In the case of a Unicode string, there is no limitation on maximum string length. In the case of an ANSI string, the maximum length of the returned string varies depending on the version of Windows—MAX_PATH prior to Windows 2000 and INFOTIPSIZE (defined in Commctrl.h) in Windows 2000 and later.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is useful when creating a link to an application that takes special flags as arguments, such as a compiler.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-getarguments">IShellLink::GetArguments</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
