---
UID: NN:mergemod.IMsmMerge
title: IMsmMerge (mergemod.h)
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.
helpviewer_keywords: ["IMsmMerge","IMsmMerge interface","IMsmMerge interface","described","_msi_imsmmerge_interface","mergemod/IMsmMerge","setup.imsmmerge_interface"]
old-location: setup\imsmmerge_interface.htm
tech.root: setup
ms.assetid: 6cb4b620-88ce-4348-ab72-6d2ed60c6298
ms.date: 12/05/2018
ms.keywords: IMsmMerge, IMsmMerge interface, IMsmMerge interface,described, _msi_imsmmerge_interface, mergemod/IMsmMerge, setup.imsmmerge_interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 1.0 or later
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
req.dll: Mergemod.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IMsmMerge
 - mergemod/IMsmMerge
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mergemod.dll
api_name:
 - IMsmMerge
---

# IMsmMerge interface


## -description

The 
<b>IMsmMerge</b> interface and the 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge2">IMsmMerge2</a> interface provide interfaces to the 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object. The 
Merge object provides access to other top-level objects. A 
<b>Merge</b> object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.

## -inheritance

The <b>IMsmMerge</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmMerge</b> also has these types of members:

