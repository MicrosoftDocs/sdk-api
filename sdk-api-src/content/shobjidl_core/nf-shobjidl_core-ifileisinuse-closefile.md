---
UID: NF:shobjidl_core.IFileIsInUse.CloseFile
title: IFileIsInUse::CloseFile (shobjidl_core.h)
description: Closes the file currently in use.
helpviewer_keywords: ["CloseFile","CloseFile method [Windows Shell]","CloseFile method [Windows Shell]","IFileIsInUse interface","IFileIsInUse interface [Windows Shell]","CloseFile method","IFileIsInUse.CloseFile","IFileIsInUse::CloseFile","_shell_IFileIsInUse_CloseFile","shell.IFileIsInUse_CloseFile","shobjidl_core/IFileIsInUse::CloseFile"]
old-location: shell\IFileIsInUse_CloseFile.htm
tech.root: shell
ms.assetid: 27338e5a-b303-4b72-b316-3059ec6f1698
ms.date: 12/05/2018
ms.keywords: CloseFile, CloseFile method [Windows Shell], CloseFile method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],CloseFile method, IFileIsInUse.CloseFile, IFileIsInUse::CloseFile, _shell_IFileIsInUse_CloseFile, shell.IFileIsInUse_CloseFile, shobjidl_core/IFileIsInUse::CloseFile
req.header: shobjidl_core.h
req.include-header: Shobjidl.h
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
 - IFileIsInUse::CloseFile
 - shobjidl_core/IFileIsInUse::CloseFile
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
 - IFileIsInUse.CloseFile
---

# IFileIsInUse::CloseFile


## -description

Closes the file currently in use.



## -returns

Type: <b>HRESULT</b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

Only files that return the <a href="/windows/desktop/api/shobjidl_core/nf-shobjidl_core-ifileisinuse-getcapabilities">capability flag</a> OF_CAP_CANCLOSE can be closed by this method. If that flag is returned, the user can be presented with a dialog box that includes a <b>Close</b> option that calls this method.
