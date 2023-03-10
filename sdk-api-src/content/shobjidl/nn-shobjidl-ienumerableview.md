---
UID: NN:shobjidl.IEnumerableView
title: IEnumerableView (shobjidl.h)
description: Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion. This interface enables clients of a view to attempt to share the view's list of folder contents.
helpviewer_keywords: ["IEnumerableView","IEnumerableView interface [Windows Shell]","IEnumerableView interface [Windows Shell]","described","_shell_IEnumerableView","shell.IEnumerableView","shobjidl/IEnumerableView"]
old-location: shell\IEnumerableView.htm
tech.root: shell
ms.assetid: 6e096f7b-b40b-45ea-a348-ddfedf5913f8
ms.date: 12/05/2018
ms.keywords: IEnumerableView, IEnumerableView interface [Windows Shell], IEnumerableView interface [Windows Shell],described, _shell_IEnumerableView, shell.IEnumerableView, shobjidl/IEnumerableView
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
 - IEnumerableView
 - shobjidl/IEnumerableView
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
 - IEnumerableView
---

# IEnumerableView interface


## -description

Exposes methods that enumerate the contents of a view and receive notification from callback upon enumeration completion. This interface enables clients of a view to attempt to share the view's list of folder contents.

## -inheritance

The <b>IEnumerableView</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IEnumerableView</b> also has these types of members:

## -remarks

<a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ifolderview">IFolderView</a> (a folder view) supports presentation of the contents of a folder, and exposes the <b>IEnumerableView</b> through <a href="/previous-versions/windows/internet-explorer/ie-developer/platform-apis/cc678966(v=vs.85)">QueryService</a> on service request SID_EnumerableView. <b>IEnumerableView</b> offers enhanced performance compared to obtaining the contents of the folder directly from the folder using <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a> (call <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-enumobjects">IShellFolder::EnumObjects</a> to return this interface). Since the view asked for the contents of the folder in order to display those contents, using <b>IEnumerableView</b> enables a client to get a copy of the work already done by <b>IFolderView</b>.

Typically, this enumeration service is compatible with most folders, and is only provided if it is safe to enumerate the contents of the view.  For example, using this service with a folder containing search results is not supported.
