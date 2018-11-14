---
UID: NF:propsys.IPropertyChangeArray.Append
title: IPropertyChangeArray::Append
author: windows-sdk-content
description: Inserts a change operation at the end of an array.
old-location: properties\IPropertyChangeArray_Append.htm
tech.root: properties
ms.assetid: 45039163-dffc-4168-9c31-786dcfdab760
ms.author: windowssdkdev
ms.date: 10/19/2018
ms.keywords: Append, Append method [Windows Properties], Append method [Windows Properties],IPropertyChangeArray interface, IPropertyChangeArray interface [Windows Properties],Append method, IPropertyChangeArray.Append, IPropertyChangeArray::Append, _shell_IPropertyChangeArray_Append, properties.IPropertyChangeArray_Append, propsys/IPropertyChangeArray::Append, shell.IPropertyChangeArray_Append
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
 - IPropertyChangeArray.Append
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- propsys.h
: 
- IPropertyChangeArray.Append
: 
---

# IPropertyChangeArray::Append


## -description


Inserts a change operation at the end of an array.


## -parameters




### -param ppropChange [in]

Type: <b><a href="shell.IPropertyChange">IPropertyChange</a>*</b>

A pointer to the interface that contains the change.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



