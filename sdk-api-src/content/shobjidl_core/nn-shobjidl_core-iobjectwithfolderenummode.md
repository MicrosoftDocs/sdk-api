---
UID: NN:shobjidl_core.IObjectWithFolderEnumMode
title: IObjectWithFolderEnumMode (shobjidl_core.h)
description: Exposes methods that get and set enumeration modes of a parsed item.
helpviewer_keywords: ["IObjectWithFolderEnumMode","IObjectWithFolderEnumMode interface [Windows Shell]","IObjectWithFolderEnumMode interface [Windows Shell]","described","_shell_IObjectWithFolderEnumMode","shell.IObjectWithFolderEnumMode","shobjidl_core/IObjectWithFolderEnumMode"]
old-location: shell\IObjectWithFolderEnumMode.htm
tech.root: shell
ms.assetid: 33838ddc-8e0e-431a-a957-40e23f0ad0c7
ms.date: 12/05/2018
ms.keywords: IObjectWithFolderEnumMode, IObjectWithFolderEnumMode interface [Windows Shell], IObjectWithFolderEnumMode interface [Windows Shell],described, _shell_IObjectWithFolderEnumMode, shell.IObjectWithFolderEnumMode, shobjidl_core/IObjectWithFolderEnumMode
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
 - IObjectWithFolderEnumMode
 - shobjidl_core/IObjectWithFolderEnumMode
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
 - IObjectWithFolderEnumMode
---

# IObjectWithFolderEnumMode interface


## -description

Exposes methods that get and set enumeration modes of a parsed item.

## -inheritance

The <b>IObjectWithFolderEnumMode</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IObjectWithFolderEnumMode</b> also has these types of members:

## -remarks

<h3><a id="When_to_Implement"></a><a id="when_to_implement"></a><a id="WHEN_TO_IMPLEMENT"></a>When to Implement</h3>
This interface is implemented as part of a Shell namespace extension, specifically the <a href="/windows/desktop/api/shobjidl_core/nn-shobjidl_core-ishellfolder">IShellFolder</a> interface.

<h3><a id="When_to_Use"></a><a id="when_to_use"></a><a id="WHEN_TO_USE"></a>When to Use</h3>
This interface is used by the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ishellfolder-parsedisplayname">IShellFolder::ParseDisplayName</a> method to retrieve the <a href="/windows/desktop/api/shobjidl_core/ne-shobjidl_core-folder_enum_mode">FOLDER_ENUM_MODE</a> value which controls the enumeration mode of the parsed item.

Items with different enumeration modes compare canonically different (SHCIDS_CANONICALONLY) because they enumerate different sets of items.
