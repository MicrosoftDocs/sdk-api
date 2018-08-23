---
UID: NF:propsys.IPropertyDescription.GetEnumTypeList
title: IPropertyDescription::GetEnumTypeList
author: windows-sdk-content
description: Gets an instance of an IPropertyEnumTypeList, which can be used to enumerate the possible values for a property.
old-location: properties\IPropertyDescription_GetEnumTypeList.htm
old-project: properties
ms.assetid: ab6c41c2-d85c-4ff9-9061-043303eb1a83
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: GetEnumTypeList, GetEnumTypeList method [Windows Properties], GetEnumTypeList method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetEnumTypeList method, IPropertyDescription.GetEnumTypeList, IPropertyDescription::GetEnumTypeList, properties.IPropertyDescription_GetEnumTypeList, propsys/IPropertyDescription::GetEnumTypeList, shell.IPropertyDescription_GetEnumTypeList, shell_IPropertyDescription_GetEnumTypeList
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: propsys.h
req.include-header: 
req.redist: 
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
tech.root: 
req.typenames: PSC_STATE
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
req.lib: 
req.dll: 
req.irql: 
req.product: ADAM
---

# IPropertyDescription::GetEnumTypeList


## -description


Gets an instance of an <a href="shell.IPropertyEnumTypeList">IPropertyEnumTypeList</a>, which can be used to enumerate the possible values for a property.


## -parameters




### -param riid




### -param ppv






#### - ppenumList [out]

Type: <b><a href="shell.IPropertyEnumTypeList">IPropertyEnumTypeList</a>**</b>

When this method returns, contains the address of an <a href="shell.IPropertyEnumTypeList">IPropertyEnumTypeList</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



