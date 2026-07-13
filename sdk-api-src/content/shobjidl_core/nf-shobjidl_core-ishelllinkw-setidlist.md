---
UID: NF:shobjidl_core.IShellLinkW.SetIDList
title: IShellLinkW::SetIDList (shobjidl_core.h)
description: Sets the pointer to an item identifier list (PIDL) for a Shell link object. (Unicode)
helpviewer_keywords: ["IShellLink interface [Windows Shell]","SetIDList method","IShellLink::SetIDList","IShellLinkA interface [Windows Shell]","SetIDList method","IShellLinkA::SetIDList","IShellLinkW interface [Windows Shell]","SetIDList method","IShellLinkW.SetIDList","IShellLinkW::SetIDList","SetIDList","SetIDList method [Windows Shell]","SetIDList method [Windows Shell]","IShellLink interface","SetIDList method [Windows Shell]","IShellLinkA interface","SetIDList method [Windows Shell]","IShellLinkW interface","_win32_IShellLink_SetIDList","shell.IShellLink_SetIDList","shobjidl_core/IShellLink::SetIDList","shobjidl_core/IShellLinkA::SetIDList","shobjidl_core/IShellLinkW::SetIDList"]
old-location: shell\IShellLink_SetIDList.htm
tech.root: shell
ms.assetid: 4c0571a5-1615-4c3f-b9a6-0667df07165b
ms.date: 12/05/2018
ms.keywords: IShellLink interface [Windows Shell],SetIDList method, IShellLink::SetIDList, IShellLinkA interface [Windows Shell],SetIDList method, IShellLinkA::SetIDList, IShellLinkW interface [Windows Shell],SetIDList method, IShellLinkW.SetIDList, IShellLinkW::SetIDList, SetIDList, SetIDList method [Windows Shell], SetIDList method [Windows Shell],IShellLink interface, SetIDList method [Windows Shell],IShellLinkA interface, SetIDList method [Windows Shell],IShellLinkW interface, _win32_IShellLink_SetIDList, shell.IShellLink_SetIDList, shobjidl_core/IShellLink::SetIDList, shobjidl_core/IShellLinkA::SetIDList, shobjidl_core/IShellLinkW::SetIDList
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
 - IShellLinkW::SetIDList
 - shobjidl_core/IShellLinkW::SetIDList
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
 - IShellLink.SetIDList
 - IShellLinkA.SetIDList
 - IShellLinkW.SetIDList
---

# IShellLinkW::SetIDList


## -description

Sets the pointer to an item identifier list (PIDL) for a Shell link object.

## -parameters

### -param pidl [in]

Type: <b>PCIDLIST_ABSOLUTE</b>

The object's fully qualified PIDL.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method is useful when an application needs to set a Shell link to an object that is not a file, such as a Control Panel application, a printer, or another computer.

