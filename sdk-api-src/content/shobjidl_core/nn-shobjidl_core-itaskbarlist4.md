---
UID: NN:shobjidl_core.ITaskbarList4
title: ITaskbarList4 (shobjidl_core.h)
description: Extends ITaskbarList3 by providing a method that allows the caller to control two property values for the tab thumbnail and peek feature.
helpviewer_keywords: ["ITaskbarList4","ITaskbarList4 interface [Windows Shell]","ITaskbarList4 interface [Windows Shell]","described","_shell_ITaskbarList4","shell.ITaskbarList4","shobjidl_core/ITaskbarList4"]
old-location: shell\ITaskbarList4.htm
tech.root: shell
ms.assetid: 7fc2c615-0bb0-4c03-9775-eee566c71088
ms.date: 12/05/2018
ms.keywords: ITaskbarList4, ITaskbarList4 interface [Windows Shell], ITaskbarList4 interface [Windows Shell],described, _shell_ITaskbarList4, shell.ITaskbarList4, shobjidl_core/ITaskbarList4
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Explorerframe.lib
req.dll: Explorerframe.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - ITaskbarList4
 - shobjidl_core/ITaskbarList4
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Explorerframe.dll
api_name:
 - ITaskbarList4
---

# ITaskbarList4 interface


## -description

Extends <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a> by providing a method that allows the caller to control two property values for the tab thumbnail and peek feature.

## -inheritance

The <b>ITaskbarList4</b> interface inherits from <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>. <b>ITaskbarList4</b> also has these types of members:

## -remarks

This interface also provides the methods of the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist">ITaskbarList</a>, <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist2">ITaskbarList2</a>, and <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a> interfaces, from which it inherits.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_TaskbarList. This interface is not implemented by third parties.

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
An implementation of this interface is provided in Windows as CLSID_TaskbarList. This interface is not implemented by third parties.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
Use the methods of this interface for the following:
                

<ul>
<li>To use the thumbnail image of the application frame window in place of the tab thumbnail in some circumstances.</li>
<li>To use the application frame window in place of the tab as the source of the tab's peek image (a full-screen view of the window in response to a mouse-over event in the thumbnail).</li>
</ul>

## -see-also

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-itaskbarlist3">ITaskbarList3</a>



<a href="/windows/desktop/shell/taskbar-extensions">Taskbar Extensions</a>
