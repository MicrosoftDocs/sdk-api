---
UID: NF:ocidl.IPropertyPageSite.GetPageContainer
title: IPropertyPageSite::GetPageContainer (ocidl.h)
description: Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages. Calling this method could potentially allow one page to navigate to another.
helpviewer_keywords: ["GetPageContainer","GetPageContainer method [COM]","GetPageContainer method [COM]","IPropertyPageSite interface","IPropertyPageSite interface [COM]","GetPageContainer method","IPropertyPageSite.GetPageContainer","IPropertyPageSite::GetPageContainer","_ctrl_ipropertypagesite_getpagecontainer","com.ipropertypagesite_getpagecontainer","ocidl/IPropertyPageSite::GetPageContainer"]
old-location: com\ipropertypagesite_getpagecontainer.htm
tech.root: com
ms.assetid: 88cbefe6-51c7-4c09-80bb-677c83f97cac
ms.date: 12/05/2018
ms.keywords: GetPageContainer, GetPageContainer method [COM], GetPageContainer method [COM],IPropertyPageSite interface, IPropertyPageSite interface [COM],GetPageContainer method, IPropertyPageSite.GetPageContainer, IPropertyPageSite::GetPageContainer, _ctrl_ipropertypagesite_getpagecontainer, com.ipropertypagesite_getpagecontainer, ocidl/IPropertyPageSite::GetPageContainer
req.header: ocidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: OCIdl.idl
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
 - IPropertyPageSite::GetPageContainer
 - ocidl/IPropertyPageSite::GetPageContainer
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - OCIdl.h
api_name:
 - IPropertyPageSite.GetPageContainer
---

# IPropertyPageSite::GetPageContainer


## -description

Retrieves a pointer to the object representing the entire property frame dialog box that contains all the pages. Calling this method could potentially allow one page to navigate to another.

However, there are no container interfaces defined for this role, so this method always fails in the property frame implementation.

## -parameters

### -param ppUnk [out]

A pointer to an <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> pointer variable that receives the interface pointer to the container object. If an error occurs, the implementation must set *<i>ppUnk</i> to <b>NULL</b>.

## -returns

This method returns E_NOTIMPL.

## -see-also

<a href="/windows/desktop/api/ocidl/nn-ocidl-ipropertypagesite">IPropertyPageSite</a>