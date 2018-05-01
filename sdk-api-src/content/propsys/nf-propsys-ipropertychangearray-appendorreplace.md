---
UID: NF:propsys.IPropertyChangeArray.AppendOrReplace
title: IPropertyChangeArray::AppendOrReplace method
author: windows-driver-content
description: Replaces the first occurrence of a change that affects the same property key as the provided change. If the property key is not already in the array, this method appends the change to the end of the array.
old-location: properties\IPropertyChangeArray_AppendOrReplace.htm
old-project: properties
ms.assetid: e4006738-d986-4fcb-899c-bbc4853ec6c1
ms.author: windowsdriverdev
ms.date: 4/5/2018
ms.keywords: AppendOrReplace method [Windows Properties], AppendOrReplace method [Windows Properties], IPropertyChangeArray interface, AppendOrReplace,IPropertyChangeArray.AppendOrReplace, IPropertyChangeArray, IPropertyChangeArray interface [Windows Properties], AppendOrReplace method, IPropertyChangeArray::AppendOrReplace, _shell_IPropertyChangeArray_AppendOrReplace, properties.IPropertyChangeArray_AppendOrReplace, propsys/IPropertyChangeArray::AppendOrReplace, shell.IPropertyChangeArray_AppendOrReplace
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
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Propsys.h
api_name:
-	IPropertyChangeArray.AppendOrReplace
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyChangeArray::AppendOrReplace method


## -description


Replaces the first occurrence of a change that affects the same property key as the provided change.  If the property key is not already in the array, this method appends the change to the end of the array.


## -parameters




### -param ppropChange [in]

Type: <b><a href="shell.IPropertyChange">IPropertyChange</a>*</b>

A pointer to the interface that contains the change


## -returns



Type: <b>HRESULT</b>

Returns <b>S_OK</b> if successful, or an error value otherwise.



