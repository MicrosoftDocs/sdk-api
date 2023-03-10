---
UID: NN:propsys.IPropertyDescriptionSearchInfo
title: IPropertyDescriptionSearchInfo (propsys.h)
description: Exposes search-related information for a property.
helpviewer_keywords: ["IPropertyDescriptionSearchInfo","IPropertyDescriptionSearchInfo interface [Windows Properties]","IPropertyDescriptionSearchInfo interface [Windows Properties]","described","_shell_IPropertyDescriptionSearchInfo","properties.IPropertyDescriptionSearchInfo","propsys/IPropertyDescriptionSearchInfo","shell.IPropertyDescriptionSearchInfo"]
old-location: properties\IPropertyDescriptionSearchInfo.htm
tech.root: properties
ms.assetid: 7bd4be80-7459-4c3d-9da4-0580995e6db6
ms.date: 12/05/2018
ms.keywords: IPropertyDescriptionSearchInfo, IPropertyDescriptionSearchInfo interface [Windows Properties], IPropertyDescriptionSearchInfo interface [Windows Properties],described, _shell_IPropertyDescriptionSearchInfo, properties.IPropertyDescriptionSearchInfo, propsys/IPropertyDescriptionSearchInfo, shell.IPropertyDescriptionSearchInfo
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
 - IPropertyDescriptionSearchInfo
 - propsys/IPropertyDescriptionSearchInfo
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
 - IPropertyDescriptionSearchInfo
---

# IPropertyDescriptionSearchInfo interface


## -description

Exposes search-related information for a property. The information provided by this interface comes from the <a href="/windows/desktop/properties/propdesc-schema-propertydescription">propertyDescription</a> schema, <a href="/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a> element for a given property. This information is used by the Windows Search Indexer. Most calling applications will not need to call this interface.

## -inheritance

The <b>IPropertyDescriptionSearchInfo</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IPropertyDescriptionSearchInfo</b> also has these types of members:

## -see-also

<a href="/windows/desktop/properties/propdesc-schema-propertydescription">propertyDescription</a>



<a href="/windows/desktop/properties/propdesc-schema-searchinfo">searchInfo</a>
