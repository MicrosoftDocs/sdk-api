---
UID: NF:propsys.IPropertyDescription.GetEnumTypeList
title: IPropertyDescription::GetEnumTypeList
author: windows-sdk-content
description: Gets an instance of an IPropertyEnumTypeList, which can be used to enumerate the possible values for a property.
old-location: properties\IPropertyDescription_GetEnumTypeList.htm
tech.root: properties
ms.assetid: ab6c41c2-d85c-4ff9-9061-043303eb1a83
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetEnumTypeList, GetEnumTypeList method [Windows Properties], GetEnumTypeList method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetEnumTypeList method, IPropertyDescription.GetEnumTypeList, IPropertyDescription::GetEnumTypeList, properties.IPropertyDescription_GetEnumTypeList, propsys/IPropertyDescription::GetEnumTypeList, shell.IPropertyDescription_GetEnumTypeList, shell_IPropertyDescription_GetEnumTypeList
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
 - IPropertyDescription.GetEnumTypeList
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescription::GetEnumTypeList


## -description


Gets an instance of an <a href="https://msdn.microsoft.com/en-us/library/Bb761483(v=VS.85).aspx">IPropertyEnumTypeList</a>, which can be used to enumerate the possible values for a property.


## -parameters




### -param riid

TBD


### -param ppv

TBD




#### - ppenumList [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761483(v=VS.85).aspx">IPropertyEnumTypeList</a>**</b>

When this method returns, contains the address of an <a href="https://msdn.microsoft.com/en-us/library/Bb761483(v=VS.85).aspx">IPropertyEnumTypeList</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



