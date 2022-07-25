---
UID: NN:shobjidl_core.IUpdateIDList
title: IUpdateIDList (shobjidl_core.h)
description: Provides a method to update the ITEMIDLIST of the child of a folder object.
helpviewer_keywords: ["IUpdateIDList","IUpdateIDList interface [Windows Shell]","IUpdateIDList interface [Windows Shell]","described","_shell_IUpdateIDList","shell.IUpdateIDList","shobjidl_core/IUpdateIDList"]
old-location: shell\IUpdateIDList.htm
tech.root: shell
ms.assetid: e6d94975-de33-497e-95a9-b89e8f8f0134
ms.date: 12/05/2018
ms.keywords: IUpdateIDList, IUpdateIDList interface [Windows Shell], IUpdateIDList interface [Windows Shell],described, _shell_IUpdateIDList, shell.IUpdateIDList, shobjidl_core/IUpdateIDList
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - IUpdateIDList
 - shobjidl_core/IUpdateIDList
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
 - IUpdateIDList
---

# IUpdateIDList interface


## -description

Provides a method to update the <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a> of the child of a folder object.

## -inheritance

The <b>IUpdateIDList</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUpdateIDList</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
Implement this interface for an <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> implementation to update the provided child <a href="/windows/desktop/api/shtypes/ns-shtypes-itemidlist">ITEMIDLIST</a>.
