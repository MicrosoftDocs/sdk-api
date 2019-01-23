---
UID: NF:propsys.IPropertyEnumType.GetEnumType
title: IPropertyEnumType::GetEnumType
author: windows-sdk-content
description: Gets an enumeration type from an enumeration information structure.
old-location: properties\IPropertyEnumType_GetEnumType.htm
tech.root: properties
ms.assetid: f73ad824-5605-4c3c-b623-debdebdf5780
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnumType, GetEnumType method [Windows Properties], GetEnumType method [Windows Properties],IPropertyEnumType interface, IPropertyEnumType interface [Windows Properties],GetEnumType method, IPropertyEnumType.GetEnumType, IPropertyEnumType::GetEnumType, PET_DEFAULTVALUE, PET_DISCRETEVALUE, PET_ENDRANGE, PET_RANGEDVALUE, _shell_IPropertyEnumType_GetEnumType, properties.IPropertyEnumType_GetEnumType, propsys/IPropertyEnumType::GetEnumType, shell.IPropertyEnumType_GetEnumType
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
 - IPropertyEnumType.GetEnumType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyEnumType::GetEnumType


## -description


Gets an enumeration type from an enumeration information structure.


## -parameters




### -param penumtype [out]

Type: <b>PROPENUMTYPE*</b>

When this method returns, contains a pointer to one of the values listed below that indicate the enumeration type.



#### PET_DISCRETEVALUE (0)

Use <a href="https://msdn.microsoft.com/en-us/library/Bb761485(v=VS.85).aspx">GetDisplayText</a> and either <a href="https://msdn.microsoft.com/en-us/library/Bb761489(v=VS.85).aspx">GetRangeMinValue</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb761491(v=VS.85).aspx">GetRangeSetValue</a>.



#### PET_RANGEDVALUE (1)

Use <a href="https://msdn.microsoft.com/en-us/library/Bb761485(v=VS.85).aspx">GetDisplayText</a> and either <a href="https://msdn.microsoft.com/en-us/library/Bb761489(v=VS.85).aspx">GetRangeMinValue</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb761491(v=VS.85).aspx">GetRangeSetValue</a>.



#### PET_DEFAULTVALUE (2)

Use <a href="https://msdn.microsoft.com/en-us/library/Bb761485(v=VS.85).aspx">GetDisplayText</a>.



#### PET_ENDRANGE (3)

Use <a href="https://msdn.microsoft.com/en-us/library/ms536253(v=VS.85).aspx">GetValue</a> or <a href="https://msdn.microsoft.com/en-us/library/Bb761489(v=VS.85).aspx">GetRangeMinValue</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For additional information, see <a href="https://msdn.microsoft.com/en-us/library/Bb773871(v=VS.85).aspx">enumeratedList</a>.



