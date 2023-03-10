---
UID: NN:shimgdata.IShellImageDataFactory
title: IShellImageDataFactory (shimgdata.h)
description: Exposes methods that create IShellImageData instances based on various image sources.
helpviewer_keywords: ["IShellImageDataFactory","IShellImageDataFactory interface [Windows Shell]","IShellImageDataFactory interface [Windows Shell]","described","_shell_IShellImageDataFactory","shell.IShellImageDataFactory","shimgdata/IShellImageDataFactory"]
old-location: shell\IShellImageDataFactory.htm
tech.root: shell
ms.assetid: c3de35de-9bf5-415c-93e9-ac0085195c27
ms.date: 12/05/2018
ms.keywords: IShellImageDataFactory, IShellImageDataFactory interface [Windows Shell], IShellImageDataFactory interface [Windows Shell],described, _shell_IShellImageDataFactory, shell.IShellImageDataFactory, shimgdata/IShellImageDataFactory
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
 - IShellImageDataFactory
 - shimgdata/IShellImageDataFactory
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
 - IShellImageDataFactory
---

# IShellImageDataFactory interface


## -description

Exposes methods that create <a href="/windows/desktop/api/shimgdata/nn-shimgdata-ishellimagedata">IShellImageData</a> instances based on various image sources.

## -inheritance

The <b>IShellImageDataFactory</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IShellImageDataFactory</b> also has these types of members:

## -remarks

This interface is not expected to be available in later versions of Windows. It is recommended that Windows GDI+ APIs be used in place of <b>IShellImageDataFactory</b> methods.

This interface was not included in a public header file prior to Windows Vista.
