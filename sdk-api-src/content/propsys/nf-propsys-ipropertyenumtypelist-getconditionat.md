---
UID: NF:propsys.IPropertyEnumTypeList.GetConditionAt
title: IPropertyEnumTypeList::GetConditionAt
author: windows-sdk-content
description: Not supported.Gets the condition at the specified index.
old-location: properties\IPropertyEnumTypeList_GetConditionAt.htm
tech.root: properties
ms.assetid: 0754ac31-09e9-429b-8ae2-58346fb50944
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: GetConditionAt, GetConditionAt method [Windows Properties], GetConditionAt method [Windows Properties],IPropertyEnumTypeList interface, IPropertyEnumTypeList interface [Windows Properties],GetConditionAt method, IPropertyEnumTypeList.GetConditionAt, IPropertyEnumTypeList::GetConditionAt, _shell_IPropertyEnumTypeList_GetConditionAt, properties.IPropertyEnumTypeList_GetConditionAt, propsys/IPropertyEnumTypeList::GetConditionAt, shell.IPropertyEnumTypeList_GetConditionAt
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: propsys.h
req.include-header: Propsys.h
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
 - propsys.h
api_name:
 - IPropertyEnumTypeList.GetConditionAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyEnumTypeList::GetConditionAt


## -description


Not supported.

Gets the condition at the specified index.


## -parameters




### -param nIndex [in]

Type: <b>UINT</b>

Index of the desired condition.


### -param riid [in]

Type: <b>REFIID</b>

A reference to the IID of the interface to retrieve.


### -param ppv [out]

Type: <b>void**</b>

When this method returns, contains the address of an <a href="https://msdn.microsoft.com/en-us/library/Bb231395(v=VS.85).aspx">ICondition</a> interface pointer.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



