---
UID: NN:shlobj.IDocViewSite
title: IDocViewSite (shlobj.h)
description: Used as a site object by the IShellView interface.
helpviewer_keywords: ["IDocViewSite","IDocViewSite interface [Windows Shell]","IDocViewSite interface [Windows Shell]","described","_win32_IDocViewSite","shell.IDocViewSite","shlobj/IDocViewSite"]
old-location: shell\IDocViewSite.htm
tech.root: shell
ms.assetid: 031e0079-842e-4357-acb2-5d1160094e18
ms.date: 12/05/2018
ms.keywords: IDocViewSite, IDocViewSite interface [Windows Shell], IDocViewSite interface [Windows Shell],described, _win32_IDocViewSite, shell.IDocViewSite, shlobj/IDocViewSite
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll (version 5.0 or later)
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IDocViewSite
 - shlobj/IDocViewSite
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
 - IDocViewSite
---

# IDocViewSite interface


## -description

<p class="CCE_Message">[This interface is supported through Windows XP Service Pack 2 (SP2) and Windows Server 2003. It might be unsupported in subsequent versions of Windows.]

Used as a site object by the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> interface.

## -inheritance

The <b>IDocViewSite</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IDocViewSite</b> also has these types of members:

## -remarks

You can call the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> method on <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellview">IShellView</a> to get a pointer to the <b>IDocViewSite</b> interface.
