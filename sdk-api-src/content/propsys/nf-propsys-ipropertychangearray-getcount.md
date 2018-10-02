---
UID: NF:propsys.IPropertyChangeArray.GetCount
title: IPropertyChangeArray::GetCount
author: windows-sdk-content
description: Gets the number of change operations in the array.
old-location: properties\IPropertyChangeArray_GetCount.htm
tech.root: properties
ms.assetid: b87db827-2eb1-4463-aa6a-10591b200adf
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: GetCount, GetCount method [Windows Properties], GetCount method [Windows Properties],IPropertyChangeArray interface, IPropertyChangeArray interface [Windows Properties],GetCount method, IPropertyChangeArray.GetCount, IPropertyChangeArray::GetCount, _shell_IPropertyChangeArray_GetCount, properties.IPropertyChangeArray_GetCount, propsys/IPropertyChangeArray::GetCount, shell.IPropertyChangeArray_GetCount
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
 - IPropertyChangeArray.GetCount
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyChangeArray::GetCount


## -description


Gets the number of change operations in the array.


## -parameters




### -param pcOperations [out]

Type: <b>UINT*</b>

A pointer to the number of change operations.


## -returns



Type: <b>HRESULT</b>

Always returns <b>S_OK</b>.



