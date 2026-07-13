---
UID: NN:winsxs.IAssemblyName
title: IAssemblyName (winsxs.h)
description: The IAssemblyName interface represents a side-by-side assembly name.
helpviewer_keywords: ["IAssemblyName","IAssemblyName interface [Side-by-side Assemblies]","IAssemblyName interface [Side-by-side Assemblies]","described","setup.iassemblyname","winsxs/IAssemblyName"]
old-location: setup\iassemblyname.htm
tech.root: setup
ms.assetid: 304b8fb3-5d17-4af0-b070-450a40dc5cc9
ms.date: 12/05/2018
ms.keywords: IAssemblyName, IAssemblyName interface [Side-by-side Assemblies], IAssemblyName interface [Side-by-side Assemblies],described, setup.iassemblyname, winsxs/IAssemblyName
req.header: winsxs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.dll: Sxs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IAssemblyName
 - winsxs/IAssemblyName
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - sxs.dll
api_name:
 - IAssemblyName
---

# IAssemblyName interface


## -description

The <b>IAssemblyName</b> interface represents a side-by-side assembly name. The side-by-side assembly name consists of a set of name-value pairs that describe the side-by-side assembly. An instance of the <b>IAssemblyName</b> interface is obtained by calling the <a href="/windows/desktop/api/winsxs/nf-winsxs-createassemblynameobject">CreateAssemblyNameObject</a> function.

## -inheritance

The <b>IAssemblyName</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IAssemblyName</b> also has these types of members:

