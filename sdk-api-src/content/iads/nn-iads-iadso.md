---
UID: NN:iads.IADsO
title: IADsO (iads.h)
description: The IADsO interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsO","IADsO interface [ADSI]","IADsO interface [ADSI]","described","_ds_iadso","adsi.iadso","iads/IADsO"]
old-location: adsi\iadso.htm
tech.root: adsi
ms.assetid: 223021ff-58ef-4762-a64a-056ccab2696c
ms.date: 12/05/2018
ms.keywords: IADsO, IADsO interface [ADSI], IADsO interface [ADSI],described, _ds_iadso, adsi.iadso, iads/IADsO
req.header: iads.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Activeds.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IADsO
 - iads/IADsO
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Activeds.dll
api_name:
 - IADsO
---

# IADsO interface


## -description

The <b>IADsO</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed for representing and managing the organization to which an account belongs. This interface is one of several that provide support for directory services to organize accounts by country/region, locality (state/city/region), organization (company), and organizational unit (department). Organization is managed by this interface, locality by the  <a href="/windows/desktop/api/iads/nn-iads-iadslocality">IADsLocality</a> interface, and organization unit by  <a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a>.
   

When a directory service provides hierarchical groupings of directory entries by country/region, locality, organization, and organization unit, you can use this, and the related interfaces, to expand the directory tree accordingly. In this case, the <b>IADsO</b> interface is implemented by an organization object that implements the  <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface as well.

## -inheritance

The <b>IADsO</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsO</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a>



<a href="/windows/desktop/api/iads/nn-iads-iadslocality">IADsLocality</a>



<a href="/windows/desktop/ADSI/iadso-property-methods">IADsO Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
