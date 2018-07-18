---
UID: NF:shappmgr.IPublishedApp2.Install2
title: IPublishedApp2::Install2
author: windows-sdk-content
description: Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.
old-location: shell\IPublishedApp2_Install2.htm
old-project: shell
ms.assetid: ce2319d0-e4e8-49a8-9803-ef386c6969a9
ms.author: windowssdkdev
ms.date: 07/16/2018
ms.keywords: IPublishedApp2 interface [Windows Shell],Install2 method, IPublishedApp2.Install2, IPublishedApp2::Install2, Install2, Install2 method [Windows Shell], Install2 method [Windows Shell],IPublishedApp2 interface, _shell_IPublishedApp2_Install2, shappmgr/IPublishedApp2::Install2, shell.IPublishedApp2_Install2
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
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
tech.root: 
req.typenames: PUBAPPINFOFLAGS
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shappmgr.h
api_name:
 - IPublishedApp2.Install2
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPublishedApp2::Install2


## -description


Installs an application published by an application publisher, while preventing multiple windows from being active on the same thread.


## -parameters




### -param pstInstall [in]

Type: <b>LPSYSTEMTIME</b>

A pointer to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure.


### -param hwndParent [in]

Type: <b>HWND</b>

A handle to the parent window.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



