---
UID: NN:shobjidl_core.IShellFolder
title: IShellFolder (shobjidl_core.h)
description: Exposed by all Shell namespace folder objects, its methods are used to manage folders.
helpviewer_keywords: ["IShellFolder","IShellFolder interface [Windows Shell]","IShellFolder interface [Windows Shell]","described","_win32_IShellFolder","_win32_IShellFolder_cpp","shell.IShellFolder","shobjidl_core/IShellFolder"]
old-location: shell\IShellFolder.htm
tech.root: shell
ms.assetid: 35190a72-298b-4554-b924-e1357b583a99
ms.date: 12/05/2018
ms.keywords: IShellFolder, IShellFolder interface [Windows Shell], IShellFolder interface [Windows Shell],described, _win32_IShellFolder, _win32_IShellFolder_cpp, shell.IShellFolder, shobjidl_core/IShellFolder
req.header: shobjidl_core.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shobjidl_core.idl
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
 - IShellFolder
 - shobjidl_core/IShellFolder
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
 - IShellFolder
---

# IShellFolder interface


## -description

Exposed by all Shell namespace folder objects, its methods are used to manage folders.

## -inheritance

The <b>IShellFolder</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellFolder</b> also has these types of members:

## -remarks

Implement this interface for objects that extend the Shell's namespace. For example, implement this interface to create a separate namespace that requires a rooted Windows Explorer or to install a new namespace directly within the hierarchy of the system namespace. You are most familiar with the contents of your namespace, so you are responsible for implementing everything needed to access your data.

Use this interface when you need to display or perform an operation on the contents of the Shell's namespace. Objects that support <b>IShellFolder</b> are usually created by other Shell folder objects. To retrieve a folder's <b>IShellFolder</b> interface, you typically start by calling <a href="/windows/desktop/api/shlobj_core/nf-shlobj_core-shgetdesktopfolder">SHGetDesktopFolder</a>. This function returns a pointer to the desktop's <b>IShellFolder</b> interface. You can then use its methods to retrieve an <b>IShellFolder</b> interface for a particular namespace folder.

<div class="alert"><b>Note</b>  <b>IShellFolder</b> methods only accept PIDLs that are relative to the folder. Some <b>IShellFolder</b> methods, such as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-getattributesof">IShellFolder::GetAttributesOf</a>, only accept single-level PIDLs. In other words, the PIDL must contain only a single <a href="/windows/desktop/api/shtypes/ns-shtypes-shitemid">SHITEMID</a> structure, plus the terminating <b>NULL</b>. When you enumerate the contents of a folder with <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ienumidlist">IEnumIDList</a>, you will receive PIDLs of this form. Other methods, such as <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-compareids">IShellFolder::CompareIDs</a>, accept multi-level PIDLs. These PIDLs can have multiple <b>SHITEMID</b> structures and identify objects one or more levels below the parent folder. Check the reference to be sure what type of PIDL can be accepted by a particular method.</div>
<div> </div>
<h3><a id="Examples"></a><a id="examples"></a><a id="EXAMPLES"></a>Examples</h3>
An example implementation of <b>IShellFolder</b> can be seen in the <a href="/previous-versions/windows/desktop/legacy/dd940360(v=vs.85)">Explorer Data Provider Sample</a> sample. The use of various <b>IShellFolder</b> methods can be found in several samples, including <a href="/previous-versions/windows/desktop/legacy/dd940361(v=vs.85)">File Operations Sample</a>.
