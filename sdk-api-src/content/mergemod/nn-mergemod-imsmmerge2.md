---
UID: NN:mergemod.IMsmMerge2
title: IMsmMerge2 (mergemod.h)
description: The IMsmMerge interface and the IMsmMerge2 interface provide interfaces to the Merge object.The IMsmMerge2 interface provides a way for the client merge tool to utilize the new configurable-module functionality.
helpviewer_keywords: ["IMsmMerge2","IMsmMerge2 interface","IMsmMerge2 interface","described","_msi_imsmmerge2_interface","mergemod/IMsmMerge2","setup.imsmmerge2_interface"]
old-location: setup\imsmmerge2_interface.htm
tech.root: setup
ms.assetid: cda5698d-4aee-4771-9989-628162b433ef
ms.date: 12/05/2018
ms.keywords: IMsmMerge2, IMsmMerge2 interface, IMsmMerge2 interface,described, _msi_imsmmerge2_interface, mergemod/IMsmMerge2, setup.imsmmerge2_interface
req.header: mergemod.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Mergemod.dll 2.0 or later
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
 - IMsmMerge2
 - mergemod/IMsmMerge2
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
 - IMsmMerge2
---

# IMsmMerge2 interface


## -description

The 
<a href="/windows/desktop/api/mergemod/nn-mergemod-imsmmerge">IMsmMerge</a> interface and the 
<b>IMsmMerge2</b> interface provide interfaces to the 
<a href="/windows/desktop/Msi/merge-object">Merge object</a>.The 
<b>IMsmMerge2</b> interface provides a way for the client merge tool to utilize the new configurable-module functionality. Mergemod.dll provides access to the extended functionality at build time through a second version of the existing CLSID. This CLSID supports existing functionality available through the 
<b>IMsmMerge</b> interface, but the default interface on the object (and the associated dual interface) is the 
<b>IMsmMerge2</b> interface instead of the 
<b>IMsmMerge</b> interface.

Requesting this interface does not commit the tool to using the new functionality. The interface supports both the standard and the "Ex" versions of the appropriate interface calls.

The 
<a href="/windows/desktop/Msi/merge-object">Merge</a> object provides access to other top-level objects. A 
Merge object must be created before loading the automation support required by COM to access the functions in Mergemod.dll.

## -inheritance

The <b>IMsmMerge2</b> interface inherits from the <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> interface. <b>IMsmMerge2</b> also has these types of members:

