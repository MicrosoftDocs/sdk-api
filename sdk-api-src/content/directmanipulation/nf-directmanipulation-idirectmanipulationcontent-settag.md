---
UID: NF:directmanipulation.IDirectManipulationContent.SetTag
title: IDirectManipulationContent::SetTag (directmanipulation.h)
description: Specifies the tag object for the content.
helpviewer_keywords: ["IDirectManipulationContent interface [Direct Manipulation]","SetTag method","IDirectManipulationContent.SetTag","IDirectManipulationContent::SetTag","SetTag","SetTag method [Direct Manipulation]","SetTag method [Direct Manipulation]","IDirectManipulationContent interface","directmanipulation.idirectmanipulationcontent_settag","directmanipulation/IDirectManipulationContent::SetTag"]
old-location: directmanipulation\idirectmanipulationcontent_settag.htm
tech.root: directmanipulation
ms.assetid: d0dce3dd-3fbf-41ea-ba70-8574701d101e
ms.date: 12/05/2018
ms.keywords: IDirectManipulationContent interface [Direct Manipulation],SetTag method, IDirectManipulationContent.SetTag, IDirectManipulationContent::SetTag, SetTag, SetTag method [Direct Manipulation], SetTag method [Direct Manipulation],IDirectManipulationContent interface, directmanipulation.idirectmanipulationcontent_settag, directmanipulation/IDirectManipulationContent::SetTag
req.header: directmanipulation.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: DirectManipulation.idl
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
 - IDirectManipulationContent::SetTag
 - directmanipulation/IDirectManipulationContent::SetTag
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - DirectManipulation.h
api_name:
 - IDirectManipulationContent.SetTag
---

# IDirectManipulationContent::SetTag


## -description

Specifies the tag object for the content.

## -parameters

### -param object [in]

The object portion of the tag.

### -param id [in]

The ID portion of the tag.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-gettag">GetTag</a> and <b>SetTag</b> are useful for associating an external COM object with the content without an external mapping between the two. They can also be used to pass information to callbacks generated for the content.

A tag is a pairing of an integer ID  (<i>id</i>) with a Component Object Model (COM) object (<i>object</i>). It can be used by an app to store and retrieve an arbitrary object associated with the content.

The <i>object</i> parameter is optional, so that the method can set just the identifier portion.

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>