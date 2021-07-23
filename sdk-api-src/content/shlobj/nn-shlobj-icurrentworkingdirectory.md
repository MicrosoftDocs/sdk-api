---
UID: NN:shlobj.ICurrentWorkingDirectory
title: ICurrentWorkingDirectory (shlobj.h)
description: Exposes methods that enable a client to retrieve or set an object's current working directory.
helpviewer_keywords: ["ICurrentWorkingDirectory","ICurrentWorkingDirectory interface [Windows Shell]","ICurrentWorkingDirectory interface [Windows Shell]","described","_win32_ICurrentWorkingDirectory","shell.ICurrentWorkingDirectory","shlobj/ICurrentWorkingDirectory"]
old-location: shell\ICurrentWorkingDirectory.htm
tech.root: shell
ms.assetid: 1fdbe616-3ca3-4f07-b89c-4c76561ba169
ms.date: 12/05/2018
ms.keywords: ICurrentWorkingDirectory, ICurrentWorkingDirectory interface [Windows Shell], ICurrentWorkingDirectory interface [Windows Shell],described, _win32_ICurrentWorkingDirectory, shell.ICurrentWorkingDirectory, shlobj/ICurrentWorkingDirectory
req.header: shlobj.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
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
 - ICurrentWorkingDirectory
 - shlobj/ICurrentWorkingDirectory
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
 - ICurrentWorkingDirectory
---

# ICurrentWorkingDirectory interface


## -description

Exposes methods that enable a client to retrieve or set an object's current working directory.

## -inheritance

The <b>ICurrentWorkingDirectory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>ICurrentWorkingDirectory</b> also has these types of members:

## -remarks

Implement this interface if your object allows clients to retrieve or set the current working directory.

Use this interface to retrieve or set the working directory of the object that exports it.
