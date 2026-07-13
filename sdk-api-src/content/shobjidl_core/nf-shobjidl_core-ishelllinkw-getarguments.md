---
UID: NF:shobjidl_core.IShellLinkW.GetArguments
title: IShellLinkW::GetArguments (shobjidl_core.h)
description: Gets the command-line arguments associated with a Shell link object. (Unicode)
helpviewer_keywords: ["GetArguments","GetArguments method [Windows Shell]","GetArguments method [Windows Shell]","IShellLink interface","GetArguments method [Windows Shell]","IShellLinkA interface","GetArguments method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetArguments method","IShellLink::GetArguments","IShellLinkA interface [Windows Shell]","GetArguments method","IShellLinkA.GetArguments","IShellLinkA::GetArguments","IShellLinkW interface [Windows Shell]","GetArguments method","IShellLinkW.GetArguments","IShellLinkW::GetArguments","_win32_IShellLink_GetArguments","shell.IShellLink_GetArguments","shobjidl_core/IShellLink::GetArguments","shobjidl_core/IShellLinkA::GetArguments","shobjidl_core/IShellLinkW::GetArguments"]
old-location: shell\IShellLink_GetArguments.htm
tech.root: shell
ms.assetid: bd807387-1998-4b38-996f-6dbacefffa48
ms.date: 12/05/2018
ms.keywords: GetArguments, GetArguments method [Windows Shell], GetArguments method [Windows Shell],IShellLink interface, GetArguments method [Windows Shell],IShellLinkA interface, GetArguments method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetArguments method, IShellLink::GetArguments, IShellLinkA interface [Windows Shell],GetArguments method, IShellLinkA.GetArguments, IShellLinkA::GetArguments, IShellLinkW interface [Windows Shell],GetArguments method, IShellLinkW.GetArguments, IShellLinkW::GetArguments, _win32_IShellLink_GetArguments, shell.IShellLink_GetArguments, shobjidl_core/IShellLink::GetArguments, shobjidl_core/IShellLinkA::GetArguments, shobjidl_core/IShellLinkW::GetArguments
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
 - IShellLinkW::GetArguments
 - shobjidl_core/IShellLinkW::GetArguments
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
 - IShellLink.GetArguments
 - IShellLinkA.GetArguments
 - IShellLinkW.GetArguments
 - IShellLinkW.GetArguments
 - IShellLinkA.GetArguments
---

# IShellLinkW::GetArguments


## -description

Gets the command-line arguments associated with a Shell link object.

## -parameters

### -param pszArgs [out]

Type: <b>LPTSTR</b>

A pointer to the buffer that, when this method returns successfully, receives the command-line arguments.

### -param cch [in]

Type: <b>int</b>

The maximum number of characters that can be copied to the buffer supplied by the <i>pszArgs</i> parameter. In the case of a Unicode string, there is no limitation on maximum string length. In the case of an ANSI string, the maximum length of the returned string varies depending on the version of Windows—MAX_PATH prior to Windows 2000 and INFOTIPSIZE (defined in Commctrl.h) in Windows 2000 and later.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

In Windows 7 and later, it is recommended that you retrieve argument strings though <a href="/windows/desktop/api/propsys/nn-propsys-ipropertystore">IPropertyStore</a> (using the <a href="/windows/desktop/properties/props-system-link-arguments">PKEY_Link_Arguments</a> value) rather than this method, which can silently truncate the string if the provided buffer is not large enough. <b>IPropertyStore</b> allocates a string of the correct size.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishelllinka">IShellLink</a>



<a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishelllinka-setarguments">IShellLink::SetArguments</a>



<b>IShellLinkA</b>



<b>IShellLinkW</b>
