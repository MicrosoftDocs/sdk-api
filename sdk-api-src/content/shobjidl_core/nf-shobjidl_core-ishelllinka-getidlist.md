---
UID: NF:shobjidl_core.IShellLinkA.GetIDList
title: IShellLinkA::GetIDList (shobjidl_core.h)
description: Gets the list of item identifiers for the target of a Shell link object. (ANSI)
helpviewer_keywords: ["GetIDList","GetIDList method [Windows Shell]","GetIDList method [Windows Shell]","IShellLink interface","GetIDList method [Windows Shell]","IShellLinkA interface","GetIDList method [Windows Shell]","IShellLinkW interface","IShellLink interface [Windows Shell]","GetIDList method","IShellLink::GetIDList","IShellLinkA interface [Windows Shell]","GetIDList method","IShellLinkA.GetIDList","IShellLinkA::GetIDList","IShellLinkW interface [Windows Shell]","GetIDList method","IShellLinkW::GetIDList","_win32_IShellLink_GetIDList","shell.IShellLink_GetIDList","shobjidl_core/IShellLink::GetIDList","shobjidl_core/IShellLinkA::GetIDList","shobjidl_core/IShellLinkW::GetIDList"]
old-location: shell\IShellLink_GetIDList.htm
tech.root: shell
ms.assetid: ae1ac1b0-bcaf-4e3b-831c-f843ae86779c
ms.date: 12/05/2018
ms.keywords: GetIDList, GetIDList method [Windows Shell], GetIDList method [Windows Shell],IShellLink interface, GetIDList method [Windows Shell],IShellLinkA interface, GetIDList method [Windows Shell],IShellLinkW interface, IShellLink interface [Windows Shell],GetIDList method, IShellLink::GetIDList, IShellLinkA interface [Windows Shell],GetIDList method, IShellLinkA.GetIDList, IShellLinkA::GetIDList, IShellLinkW interface [Windows Shell],GetIDList method, IShellLinkW::GetIDList, _win32_IShellLink_GetIDList, shell.IShellLink_GetIDList, shobjidl_core/IShellLink::GetIDList, shobjidl_core/IShellLinkA::GetIDList, shobjidl_core/IShellLinkW::GetIDList
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
 - IShellLinkA::GetIDList
 - shobjidl_core/IShellLinkA::GetIDList
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
 - IShellLink.GetIDList
 - IShellLinkA.GetIDList
 - IShellLinkW.GetIDList
---

# IShellLinkA::GetIDList


## -description

Gets the list of item identifiers for the target of a Shell link object.

## -parameters

### -param ppidl [out]

Type: <b>PIDLIST_ABSOLUTE*</b>

When this method returns, contains the address of a PIDL.

## -returns

Type: <b>HRESULT</b>

Returns S_OK if the operation is successful and one or more valid PIDLs is retrieved. If the operation is successful but no PIDLs are retrieved, it returns S_FALSE with <i>ppidl</i> set to <b>NULL</b>. Otherwise, it returns a standard error value.

