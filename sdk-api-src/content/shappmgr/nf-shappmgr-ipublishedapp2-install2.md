---
UID: NF:shappmgr.IPublishedApp2.Install2
title: IPublishedApp2::Install2 (shappmgr.h)
description: Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.
helpviewer_keywords: ["IPublishedApp2 interface [Windows Shell]","Install2 method","IPublishedApp2.Install2","IPublishedApp2::Install2","Install2","Install2 method [Windows Shell]","Install2 method [Windows Shell]","IPublishedApp2 interface","_shell_IPublishedApp2_Install2","shappmgr/IPublishedApp2::Install2","shell.IPublishedApp2_Install2"]
old-location: shell\IPublishedApp2_Install2.htm
tech.root: shell
ms.assetid: ce2319d0-e4e8-49a8-9803-ef386c6969a9
ms.date: 12/05/2018
ms.keywords: IPublishedApp2 interface [Windows Shell],Install2 method, IPublishedApp2.Install2, IPublishedApp2::Install2, Install2, Install2 method [Windows Shell], Install2 method [Windows Shell],IPublishedApp2 interface, _shell_IPublishedApp2_Install2, shappmgr/IPublishedApp2::Install2, shell.IPublishedApp2_Install2
req.header: shappmgr.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shappmgr.idl
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
 - IPublishedApp2::Install2
 - shappmgr/IPublishedApp2::Install2
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp2.Install2
---

# IPublishedApp2::Install2


## -description

Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.

## -parameters

### -param pstInstall [in]

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="/windows/desktop/api/minwinbase/ns-minwinbase-systemtime">SYSTEMTIME</a> structure.

### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the parent window.

## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.