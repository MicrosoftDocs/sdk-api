---
UID: NN:directml.IDMLObject
title: IDMLObject
author: windows-sdk-content
description: An interface from which IDMLDevice and IDMLDeviceChild inherit directly (and all other interfaces, indirectly).
old-location: direct3d12\idmlobject.htm
tech.root: direct3d12
ms.assetid: E41D99AF-838B-43D3-AD3F-A2F7CA85C714
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: IDMLObject, IDMLObject interface, IDMLObject interface,described, direct3d12.idmlobject, directml/IDMLObject
ms.topic: interface
f1_keywords: ["directml/IDMLObject"]
req.header: directml.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: 
req.target-min-winversvr: 
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectML.h
api_name:
 - IDMLObject
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IDMLObject interface

## -description

An interface from which [IDMLDevice](/windows/desktop/api/directml/nn-directml-idmldevice) and [IDMLDeviceChild](/windows/desktop/api/directml/nn-directml-idmldevicechild) inherit directly (and all other interfaces, indirectly). Consequently, it provides methods common to all DirectML interfaces, specifically methods to associate private data, and to annotate object names. The <b>IDMLObject</b> interface inherits from the [IUnknown](/windows/desktop/api/unknwn/nn-unknwn-iunknown) interface.
