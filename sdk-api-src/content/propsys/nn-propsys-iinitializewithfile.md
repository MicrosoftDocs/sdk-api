---
UID: NN:propsys.IInitializeWithFile
title: IInitializeWithFile (propsys.h)
description: Exposes a method to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with a file path.
helpviewer_keywords: ["IInitializeWithFile","IInitializeWithFile interface [Windows Shell]","IInitializeWithFile interface [Windows Shell]","described","propsys/IInitializeWithFile","shell.IInitializeWithFile","shell_IInitializeWithFile"]
old-location: shell\IInitializeWithFile.htm
tech.root: shell
ms.assetid: 323181ab-1dc2-4b2a-a91f-3eccd7968bcd
ms.date: 12/05/2018
ms.keywords: IInitializeWithFile, IInitializeWithFile interface [Windows Shell], IInitializeWithFile interface [Windows Shell],described, propsys/IInitializeWithFile, shell.IInitializeWithFile, shell_IInitializeWithFile
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Propsys.idl
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
 - IInitializeWithFile
 - propsys/IInitializeWithFile
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IInitializeWithFile
---

# IInitializeWithFile interface


## -description

Exposes a method to initialize a handler, such as a property handler, thumbnail handler, or preview handler, with a file path.

## -inheritance

The <b>IInitializeWithFile</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IInitializeWithFile</b> also has these types of members:

## -remarks

Whenever possible, it is recommended that initialization be done through a stream using <a href="/windows/desktop/api/propsys/nn-propsys-iinitializewithstream">IInitializeWithStream</a>. Benefits of this include increased security and stability.
