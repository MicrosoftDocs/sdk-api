---
UID: NN:shimgdata.IShellImageDataAbort
title: IShellImageDataAbort (shimgdata.h)
description: Exposes a single method used to abort IShellImageData processes.
helpviewer_keywords: ["IShellImageDataAbort","IShellImageDataAbort interface [Windows Shell]","IShellImageDataAbort interface [Windows Shell]","described","_shell_IShellImageDataAbort","shell.IShellImageDataAbort","shimgdata/IShellImageDataAbort"]
old-location: shell\IShellImageDataAbort.htm
tech.root: shell
ms.assetid: 98a79c41-a384-4486-af51-a33cd5f0750e
ms.date: 12/05/2018
ms.keywords: IShellImageDataAbort, IShellImageDataAbort interface [Windows Shell], IShellImageDataAbort interface [Windows Shell],described, _shell_IShellImageDataAbort, shell.IShellImageDataAbort, shimgdata/IShellImageDataAbort
req.header: shimgdata.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Shimgdata.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Shell32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IShellImageDataAbort
 - shimgdata/IShellImageDataAbort
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
 - IShellImageDataAbort
---

# IShellImageDataAbort interface


## -description

Exposes a single method used to abort <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> processes.

## -inheritance

The <b>IShellImageDataAbort</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageDataAbort</b> also has these types of members:

## -remarks

This interface is not expected to be available in later versions of Windows. It is recommended that Windows GDI+ APIs be used in place of <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> methods.

This interface was not included in a public header file prior to Windows Vista.
