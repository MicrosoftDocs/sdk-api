---
UID: NF:propsys.IPropertyChangeArray.AppendOrReplace
title: IPropertyChangeArray::AppendOrReplace
author: windows-sdk-content
description: Replaces the first occurrence of a change that affects the same property key as the provided change. If the property key is not already in the array, this method appends the change to the end of the array.
old-location: properties\IPropertyChangeArray_AppendOrReplace.htm
tech.root: properties
ms.assetid: e4006738-d986-4fcb-899c-bbc4853ec6c1
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: AppendOrReplace, AppendOrReplace method [Windows Properties], AppendOrReplace method [Windows Properties],IPropertyChangeArray interface, IPropertyChangeArray interface [Windows Properties],AppendOrReplace method, IPropertyChangeArray.AppendOrReplace, IPropertyChangeArray::AppendOrReplace, _shell_IPropertyChangeArray_AppendOrReplace, properties.IPropertyChangeArray_AppendOrReplace, propsys/IPropertyChangeArray::AppendOrReplace, shell.IPropertyChangeArray_AppendOrReplace
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
 - IPropertyChangeArray.AppendOrReplace
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyChangeArray::AppendOrReplace


## -description


Replaces the first occurrence of a change that affects the same property key as the provided change.  If the property key is not already in the array, this method appends the change to the end of the array.


## -parameters




### -param ppropChange [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb775244(v=VS.85).aspx">IPropertyChange</a>*</b>

A pointer to the interface that contains the change


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.



