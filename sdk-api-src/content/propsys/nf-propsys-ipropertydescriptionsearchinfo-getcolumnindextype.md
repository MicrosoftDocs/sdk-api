---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetColumnIndexType
title: IPropertyDescriptionSearchInfo::GetColumnIndexType (propsys.h)

description: Determines the how the current property is indexed.
old-location: properties\IPropertyDescriptionSearchInfo_GetColumnIndexType.htm
tech.root: properties
ms.assetid: a519cfe5-e9ae-48ef-9538-a03ddc538efd

ms.date: 12/05/2018
ms.keywords: GetColumnIndexType, GetColumnIndexType method [Windows Properties], GetColumnIndexType method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetColumnIndexType method, IPropertyDescriptionSearchInfo.GetColumnIndexType, IPropertyDescriptionSearchInfo::GetColumnIndexType, _shell_IPropertyDescriptionSearchInfo_GetColumnIndexType, properties.IPropertyDescriptionSearchInfo_GetColumnIndexType, propsys/IPropertyDescriptionSearchInfo::GetColumnIndexType, shell.IPropertyDescriptionSearchInfo_GetColumnIndexType
ms.topic: method
f1_keywords: 
 - "propsys/IPropertyDescriptionSearchInfo.GetColumnIndexType"
dev_langs:
 - c++
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Propsys.h
api_name:
 - IPropertyDescriptionSearchInfo.GetColumnIndexType
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IPropertyDescriptionSearchInfo::GetColumnIndexType


## -description


Determines the how the current property is indexed.


## -parameters




### -param ppdciType [out]

Type: <b><a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-propdesc_columnindex_type">PROPDESC_COLUMNINDEX_TYPE</a>*</b>

When this method returns successfully, contains a pointer to a <a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-propdesc_columnindex_type">PROPDESC_COLUMNINDEX_TYPE</a> constant. This constant describes whether the property is indexed and if so, if it is indexed in memory or on disk.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://docs.microsoft.com/windows/desktop/api/propsys/nn-propsys-ipropertydescriptionsearchinfo">IPropertyDescriptionSearchInfo</a>



<a href="https://docs.microsoft.com/windows/desktop/api/propsys/ne-propsys-propdesc_columnindex_type">PROPDESC_COLUMNINDEX_TYPE</a>
 

 

