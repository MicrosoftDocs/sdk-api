---
UID: NN:shobjidl_core.INameSpaceTreeControlFolderCapabilities
title: INameSpaceTreeControlFolderCapabilities (shobjidl_core.h)
description: Exposes a single method that retrieves the status of a folder's System.IsPinnedToNameSpaceTree filtering support.
helpviewer_keywords: ["INameSpaceTreeControlFolderCapabilities","INameSpaceTreeControlFolderCapabilities interface [Windows Shell]","INameSpaceTreeControlFolderCapabilities interface [Windows Shell]","described","_shell_INameSpaceTreeControlFolderCapabilities","shell.INameSpaceTreeControlFolderCapabilities","shobjidl_core/INameSpaceTreeControlFolderCapabilities"]
old-location: shell\INameSpaceTreeControlFolderCapabilities.htm
tech.root: shell
ms.assetid: 2a5580f6-42cb-46c7-9507-a59d36b2cd91
ms.date: 12/05/2018
ms.keywords: INameSpaceTreeControlFolderCapabilities, INameSpaceTreeControlFolderCapabilities interface [Windows Shell], INameSpaceTreeControlFolderCapabilities interface [Windows Shell],described, _shell_INameSpaceTreeControlFolderCapabilities, shell.INameSpaceTreeControlFolderCapabilities, shobjidl_core/INameSpaceTreeControlFolderCapabilities
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
 - INameSpaceTreeControlFolderCapabilities
 - shobjidl_core/INameSpaceTreeControlFolderCapabilities
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
 - INameSpaceTreeControlFolderCapabilities
---

# INameSpaceTreeControlFolderCapabilities interface


## -description

Exposes a single method that retrieves the status of a folder's <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System.IsPinnedToNameSpaceTree</a> filtering support.

## -inheritance

The <b>INameSpaceTreeControlFolderCapabilities</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>INameSpaceTreeControlFolderCapabilities</b> also has these types of members:

## -remarks

The namespace tree control checks all the nodes it enumerates to see if they support filtering. This is done by retrieving the <a href="/windows/desktop/properties/props-system-ispinnedtonamespacetree">System.IsPinnedToNameSpaceTree</a> property for the shell folders that support this interface. Nodes that do not support this interface do not have filtering support and are shown by default.

Use this interface to retrieve the filtering support status of a shell folder.
