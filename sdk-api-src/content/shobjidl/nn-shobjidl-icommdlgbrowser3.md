---
UID: NN:shobjidl.ICommDlgBrowser3
title: ICommDlgBrowser3 (shobjidl.h)
description: Extends the capabilities of ICommDlgBrowser2, and used by the common file dialog boxes when they host a Shell browser.
helpviewer_keywords: ["ICommDlgBrowser3","ICommDlgBrowser3 interface [Windows Shell]","ICommDlgBrowser3 interface [Windows Shell]","described","_shell_ICommDlgBrowser3","shell.ICommDlgBrowser3","shobjidl/ICommDlgBrowser3"]
old-location: shell\ICommDlgBrowser3.htm
tech.root: shell
ms.assetid: c9286061-8ac8-452b-9204-193bc6b571cb
ms.date: 12/05/2018
ms.keywords: ICommDlgBrowser3, ICommDlgBrowser3 interface [Windows Shell], ICommDlgBrowser3 interface [Windows Shell],described, _shell_ICommDlgBrowser3, shell.ICommDlgBrowser3, shobjidl/ICommDlgBrowser3
req.header: shobjidl.h
req.include-header: 
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
 - ICommDlgBrowser3
 - shobjidl/ICommDlgBrowser3
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Shobjidl.h
api_name:
 - ICommDlgBrowser3
---

# ICommDlgBrowser3 interface


## -description

Extends the capabilities of <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>, and used by the common file dialog boxes when they host a Shell browser.

## -inheritance

The <b>ICommDlgBrowser3</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a>. <b>ICommDlgBrowser3</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser">ICommDlgBrowser</a> and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a> interfaces, from which it inherits.

A pointer to <b>ICommDlgBrowser3</b> can be obtained by calling <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-queryinterface(q)">QueryInterface</a> on the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-icommdlgbrowser2">ICommDlgBrowser2</a> object.
