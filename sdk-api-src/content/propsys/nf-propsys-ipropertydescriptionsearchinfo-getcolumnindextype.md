---
UID: NF:propsys.IPropertyDescriptionSearchInfo.GetColumnIndexType
title: IPropertyDescriptionSearchInfo::GetColumnIndexType
author: windows-sdk-content
description: Determines the how the current property is indexed.
old-location: properties\IPropertyDescriptionSearchInfo_GetColumnIndexType.htm
tech.root: properties
ms.assetid: a519cfe5-e9ae-48ef-9538-a03ddc538efd
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: GetColumnIndexType, GetColumnIndexType method [Windows Properties], GetColumnIndexType method [Windows Properties],IPropertyDescriptionSearchInfo interface, IPropertyDescriptionSearchInfo interface [Windows Properties],GetColumnIndexType method, IPropertyDescriptionSearchInfo.GetColumnIndexType, IPropertyDescriptionSearchInfo::GetColumnIndexType, _shell_IPropertyDescriptionSearchInfo_GetColumnIndexType, properties.IPropertyDescriptionSearchInfo_GetColumnIndexType, propsys/IPropertyDescriptionSearchInfo::GetColumnIndexType, shell.IPropertyDescriptionSearchInfo_GetColumnIndexType
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescriptionSearchInfo::GetColumnIndexType


## -description


Determines the how the current property is indexed.


## -parameters




### -param ppdciType [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762587(v=VS.85).aspx">PROPDESC_COLUMNINDEX_TYPE</a>*</b>

When this method returns successfully, contains a pointer to a <a href="https://msdn.microsoft.com/en-us/library/Bb762587(v=VS.85).aspx">PROPDESC_COLUMNINDEX_TYPE</a> constant. This constant describes whether the property is indexed and if so, if it is indexed in memory or on disk.
                


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761505(v=VS.85).aspx">IPropertyDescriptionSearchInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/Bb762587(v=VS.85).aspx">PROPDESC_COLUMNINDEX_TYPE</a>
 

 

