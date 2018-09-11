---
UID: NF:propsys.IPropertyChangeArray.RemoveAt
title: IPropertyChangeArray::RemoveAt
author: windows-sdk-content
description: Removes a specified change.
old-location: properties\IPropertyChangeArray_RemoveAt.htm
tech.root: properties
ms.assetid: 59d98675-c934-4f2d-8018-f581017d5441
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: IPropertyChangeArray interface [Windows Properties],RemoveAt method, IPropertyChangeArray.RemoveAt, IPropertyChangeArray::RemoveAt, RemoveAt, RemoveAt method [Windows Properties], RemoveAt method [Windows Properties],IPropertyChangeArray interface, _shell_IPropertyChangeArray_RemoveAt, properties.IPropertyChangeArray_RemoveAt, propsys/IPropertyChangeArray::RemoveAt, shell.IPropertyChangeArray_RemoveAt
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
 - IPropertyChangeArray.RemoveAt
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyChangeArray::RemoveAt


## -description


Removes a specified change.


## -parameters




### -param iIndex [in]

Type: <b>UINT</b>

The index of the change to remove.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.



