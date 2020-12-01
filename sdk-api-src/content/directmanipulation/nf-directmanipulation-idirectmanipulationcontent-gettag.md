---
UID: NF:directmanipulation.IDirectManipulationContent.GetTag
title: IDirectManipulationContent::GetTag (directmanipulation.h)
description: Retrieves the tag object set on this content.
helpviewer_keywords: ["GetTag","GetTag method [Direct Manipulation]","GetTag method [Direct Manipulation]","IDirectManipulationContent interface","IDirectManipulationContent interface [Direct Manipulation]","GetTag method","IDirectManipulationContent.GetTag","IDirectManipulationContent::GetTag","directmanipulation.idirectmanipulationcontent_gettag","directmanipulation/IDirectManipulationContent::GetTag"]
old-location: directmanipulation\idirectmanipulationcontent_gettag.htm
tech.root: directmanipulation
ms.assetid: 11acda14-3932-43e4-b45e-e129886c354f
ms.date: 12/05/2018
ms.keywords: GetTag, GetTag method [Direct Manipulation], GetTag method [Direct Manipulation],IDirectManipulationContent interface, IDirectManipulationContent interface [Direct Manipulation],GetTag method, IDirectManipulationContent.GetTag, IDirectManipulationContent::GetTag, directmanipulation.idirectmanipulationcontent_gettag, directmanipulation/IDirectManipulationContent::GetTag
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
 - IDirectManipulationContent::GetTag
 - directmanipulation/IDirectManipulationContent::GetTag
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
 - IDirectManipulationContent.GetTag
---

# IDirectManipulationContent::GetTag


## -description

Retrieves the tag object set on this content.

## -parameters

### -param riid [in]

A reference to the identifier of the interface to use. The tag object typically implements this interface.

### -param object [out, optional]

The tag object.

### -param id [out, optional]

The ID portion of the tag.

## -returns

If the method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

<b>GetTag</b> and <a href="/previous-versions/windows/desktop/api/directmanipulation/nf-directmanipulation-idirectmanipulationcontent-settag">SetTag</a> are useful for associating an external COM object with the content without an external mapping between the two. They can also be used to pass information to callbacks generated for the content.

<b>GetTag</b> queries the tag value for the specified interface and returns a pointer to that interface.

A tag is a pairing of an integer ID (<i>id</i>) with a Component Object Model (COM) object (<i>object</i>). It can be used by an app to identify a motion.
The parameters are optional, so that the method can return both parts of the tag, the identifier portion, or the tag object.




#### Examples

The following example shows the syntax for this method.


```
IUnknown* pObject;
UINT32 id;

HRESULT hr = pContent->GetTag(IID_PPV_ARGS(&pObject), &id);

```

## -see-also

<a href="/previous-versions/windows/desktop/api/directmanipulation/nn-directmanipulation-idirectmanipulationcontent">IDirectManipulationContent</a>