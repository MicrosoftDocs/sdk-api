---
UID: NF:propsys.IPropertyChange.ApplyToPropVariant
title: IPropertyChange::ApplyToPropVariant
author: windows-sdk-content
description: Applies a change to a property value.
old-location: properties\IPropertyChange_ApplyToPropVariant.htm
tech.root: properties
ms.assetid: 7d7b6de5-0ed9-44fc-b2b3-c0f4cd8bf9c5
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: ApplyToPropVariant, ApplyToPropVariant method [Windows Properties], ApplyToPropVariant method [Windows Properties],IPropertyChange interface, IPropertyChange interface [Windows Properties],ApplyToPropVariant method, IPropertyChange.ApplyToPropVariant, IPropertyChange::ApplyToPropVariant, _shell_IPropertyChange_ApplyToPropVariant, properties.IPropertyChange_ApplyToPropVariant, propsys/IPropertyChange::ApplyToPropVariant, shell.IPropertyChange_ApplyToPropVariant
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
 - IPropertyChange.ApplyToPropVariant
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyChange::ApplyToPropVariant


## -description


Applies a change to a property value.


## -parameters




### -param propvarIn [in]

Type: <b>REFPROPVARIANT</b>

A reference to a source <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


### -param ppropvarOut [out]

Type: <b><a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a>*</b>

A pointer to a changed <a href="https://msdn.microsoft.com/e86cc279-826d-4767-8d96-fc8280060ea1">PROPVARIANT</a> structure.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="shell.IPropertyChange">IPropertyChange</a>



<a href="shell.PSCreateSimplePropertyChange">PSCreateSimplePropertyChange</a>
 

 

