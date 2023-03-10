---
UID: NN:iads.IADsLocality
title: IADsLocality (iads.h)
description: The IADsLocality interface is a dual interface that inherits from IADs.
helpviewer_keywords: ["IADsLocality","IADsLocality interface [ADSI]","IADsLocality interface [ADSI]","described","_ds_iadslocality","adsi.iadslocality","iads/IADsLocality"]
old-location: adsi\iadslocality.htm
tech.root: adsi
ms.assetid: fec0c8c2-b17f-49a0-9c97-260c98e71604
ms.date: 12/05/2018
ms.keywords: IADsLocality, IADsLocality interface [ADSI], IADsLocality interface [ADSI],described, _ds_iadslocality, adsi.iadslocality, iads/IADsLocality
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
 - IADsLocality
 - iads/IADsLocality
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
 - IADsLocality
---

# IADsLocality interface


## -description

The <b>IADsLocality</b> interface is a dual interface that inherits from <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. It is designed to represent the geographical location, or region, of a directory entity. This interface is one of several that provide support for directory services to organize accounts by country/region, locality (state/city/region), organization (company), or organizational unit (department). This interface manages locality, the  <a href="/windows/desktop/api/iads/nn-iads-iadso">IADsO</a> interface manages organization, and the  <a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a> interface manages the organization unit.
   

When a directory service provides hierarchical groupings of directory entries by country/region, locality, organization, or organization unit, you can use this and the related interfaces to expand the directory tree accordingly. In this case, the <b>IADsLocality</b> interface is implemented by a locality object that implements the <a href="/windows/desktop/api/iads/nn-iads-iadscontainer">IADsContainer</a> interface.

## -inheritance

The <b>IADsLocality</b> interface inherits from <a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a> and <a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>. <b>IADsLocality</b> also has these types of members:

## -see-also

<a href="/windows/desktop/api/iads/nn-iads-iads">IADs</a>



<a href="/windows/desktop/ADSI/iadslocality-property-methods">IADsLocality Property Methods</a>



<a href="/windows/desktop/api/iads/nn-iads-iadso">IADsO</a>



<a href="/windows/desktop/api/iads/nn-iads-iadsou">IADsOU</a>



<a href="/previous-versions/windows/desktop/api/oaidl/nn-oaidl-idispatch">IDispatch</a>
