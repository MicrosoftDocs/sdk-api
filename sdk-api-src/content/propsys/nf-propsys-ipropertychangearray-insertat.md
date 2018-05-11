---
UID: NF:propsys.IPropertyChangeArray.InsertAt
title: IPropertyChangeArray::InsertAt
author: windows-driver-content
description: Inserts a change operation into an array at the specified position.
old-location: properties\IPropertyChangeArray_InsertAt.htm
old-project: properties
ms.assetid: e50a0642-ff01-4cf7-940e-0241b3dc8604
ms.author: windowsdriverdev
ms.date: 5/8/2018
ms.keywords: IPropertyChangeArray interface [Windows Properties],InsertAt method, IPropertyChangeArray.InsertAt, IPropertyChangeArray::InsertAt, InsertAt, InsertAt method [Windows Properties], InsertAt method [Windows Properties],IPropertyChangeArray interface, _shell_IPropertyChangeArray_InsertAt, properties.IPropertyChangeArray_InsertAt, propsys/IPropertyChangeArray::InsertAt, shell.IPropertyChangeArray_InsertAt
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
-	IPropertyChangeArray.InsertAt
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Rights Management Services client 1.0 SP2 or later
---

# IPropertyChangeArray::InsertAt


## -description


Inserts a change operation into an array at the specified position.


## -parameters




### -param iIndex [in]

Type: <b>UINT</b>

The index at which the change is inserted.


### -param ppropChange [in]

Type: <b><a href="shell.IPropertyChange">IPropertyChange</a>*</b>

A pointer to the interface that contains the change.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



