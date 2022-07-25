---
UID: NF:shobjidl_core.IKnownFolder.GetRedirectionCapabilities
title: IKnownFolder::GetRedirectionCapabilities (shobjidl_core.h)
description: Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.
helpviewer_keywords: ["GetRedirectionCapabilities","GetRedirectionCapabilities method [Windows Shell]","GetRedirectionCapabilities method [Windows Shell]","IKnownFolder interface","IKnownFolder interface [Windows Shell]","GetRedirectionCapabilities method","IKnownFolder.GetRedirectionCapabilities","IKnownFolder::GetRedirectionCapabilities","_shell_IKnownFolder_GetRedirectionCapabilities","shell.IKnownFolder_GetRedirectionCapabilities","shobjidl_core/IKnownFolder::GetRedirectionCapabilities"]
old-location: shell\IKnownFolder_GetRedirectionCapabilities.htm
tech.root: shell
ms.assetid: 5abc4944-1fd7-400a-817d-b58a7f4989ea
ms.date: 12/05/2018
ms.keywords: GetRedirectionCapabilities, GetRedirectionCapabilities method [Windows Shell], GetRedirectionCapabilities method [Windows Shell],IKnownFolder interface, IKnownFolder interface [Windows Shell],GetRedirectionCapabilities method, IKnownFolder.GetRedirectionCapabilities, IKnownFolder::GetRedirectionCapabilities, _shell_IKnownFolder_GetRedirectionCapabilities, shell.IKnownFolder_GetRedirectionCapabilities, shobjidl_core/IKnownFolder::GetRedirectionCapabilities
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
 - IKnownFolder::GetRedirectionCapabilities
 - shobjidl_core/IKnownFolder::GetRedirectionCapabilities
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
 - IKnownFolder.GetRedirectionCapabilities
---

# IKnownFolder::GetRedirectionCapabilities


## -description

Gets a value that states whether the known folder can have its path set to a new value or what specific restrictions or prohibitions are placed on that redirection.

## -parameters

### -param pCapabilities [out]

Type: <b><a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities">KF_REDIRECTION_CAPABILITIES</a>*</b>

When this method returns, contains a pointer to a <a href="/windows/win32/api/shobjidl_core/ne-shobjidl_core-_kf_redirection_capabilities">KF_REDIRECTION_CAPABILITIES</a> value that indicates the redirection capabilities for this folder.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-iknownfolder">IKnownFolder</a>



<a href="/previous-versions/windows/desktop/legacy/dd940364(v=vs.85)">Known Folders Sample</a>