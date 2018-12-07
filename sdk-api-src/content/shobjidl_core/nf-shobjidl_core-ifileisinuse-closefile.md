---
UID: NF:shobjidl_core.IFileIsInUse.CloseFile
title: IFileIsInUse::CloseFile
author: windows-sdk-content
description: Closes the file currently in use.
old-location: shell\IFileIsInUse_CloseFile.htm
tech.root: shell
ms.assetid: 27338e5a-b303-4b72-b316-3059ec6f1698
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: CloseFile, CloseFile method [Windows Shell], CloseFile method [Windows Shell],IFileIsInUse interface, IFileIsInUse interface [Windows Shell],CloseFile method, IFileIsInUse.CloseFile, IFileIsInUse::CloseFile, _shell_IFileIsInUse_CloseFile, shell.IFileIsInUse_CloseFile, shobjidl_core/IFileIsInUse::CloseFile
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - shobjidl_core.h
api_name:
 - IFileIsInUse.CloseFile
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IFileIsInUse::CloseFile


## -description


Closes the file currently in use.


## -parameters






## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



Only files that return the <a href="https://msdn.microsoft.com/d2ce674a-4c06-401d-bfb0-bc2a086ef89c">capability flag</a> OF_CAP_CANCLOSE can be closed by this method. If that flag is returned, the user can be presented with a dialog box that includes a <b>Close</b> option that calls this method.



