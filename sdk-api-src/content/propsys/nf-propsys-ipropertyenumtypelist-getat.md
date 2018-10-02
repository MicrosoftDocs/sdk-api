---
UID: NF:propsys.IPropertyEnumTypeList.GetAt
title: IPropertyEnumTypeList::GetAt
author: windows-sdk-content
description: Gets the IPropertyEnumType object at the specified index in the list.
old-location: properties\IPropertyEnumTypeList_GetAt.htm
tech.root: properties
ms.assetid: 1713d16f-58d9-46f9-9795-4e05ff257901
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetAt, GetAt method [Windows Properties], GetAt method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],GetAt method, IPropertyEnumTypeList.GetAt, IPropertyEnumTypeList::GetAt, _shell_IPropertyEnumTypeList_GetAt, properties.IPropertyEnumTypeList_GetAt, propsys/IPropertyEnumTypeList::GetAt, shell.IPropertyEnumTypeList_GetAt
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
 - IPropertyEnumTypeList.GetAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyEnumTypeList::GetAt


## -description


Gets the <a href="https://msdn.microsoft.com/en-us/library/Bb761495(v=VS.85).aspx">IPropertyEnumType</a> object at the specified index in the list.


## -parameters




### -param itype [in]

Type: <b>UINT</b>

The index of the object in the list.


### -param riid

TBD


### -param ppv

TBD




#### - ppenumtype [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb761495(v=VS.85).aspx">IPropertyEnumType</a>**</b>

When this method returns, contains the address of an <a href="https://msdn.microsoft.com/en-us/library/Bb761495(v=VS.85).aspx">IPropertyEnumType</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



