---
UID: NF:propsys.PSPropertyBag_WriteUnknown
title: PSPropertyBag_WriteUnknown function
author: windows-driver-content
description: Writes a property of an unknown data value in a property bag.
old-location: properties\PSPropertyBag_WriteUnknown.htm
old-project: properties
ms.assetid: D96643E7-9A14-4410-BD2C-A264B74E0590
ms.author: windowsdriverdev
ms.date: 3/27/2018
ms.keywords: PSPropertyBag_WriteUnknown, PSPropertyBag_WriteUnknown function [Windows Properties], properties.PSPropertyBag_WriteUnknown, propsys/PSPropertyBag_WriteUnknown, shell.PSPropertyBag_WriteUnknown, shell_PSPropertyBag_WriteUnknown
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: propsys.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: PSC_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Propsys.dll
api_name:
-	PSPropertyBag_WriteUnknown
product: Windows
targetos: Windows
req.lib: Propsys.lib
req.dll: Propsys.dll (version 6.0 or later)
req.irql: 
req.product: Compute Cluster Pack Client Utilities
---

# PSPropertyBag_WriteUnknown function


## -description


Writes a property of an unknown data value in a property bag.


## -parameters




### -param propBag [in]

Type: <b><a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a>*</b>

A pointer to an <a href="_inet_IPropertyBag_Interface_cpp">IPropertyBag</a> object that represents the property bag in which the property is stored.


### -param propName [in]

Type: <b>LPCWSTR</b>

A pointer to a null-terminated property name string.


### -param punk [in]

Type: <b><a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a>*</b>

A pointer to an <a href="https://msdn.microsoft.com/33f1d79a-33fc-4ce5-a372-e08bda378332">IUnknown</a> derived interface that copies the specified property of an unknown data value in a property bag.


## -returns



Type: <b>HRESULT</b>

If this function succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The property bag property function API converts between window types and the <b>VARIANT</b> type that is used to express values in a property bag. Doing so eases property bag usage, simplifies applications, and avoids common coding errors.




## -see-also




<a href="shell.PSPropertyBag_ReadUnknown">PSPropertyBag_ReadUnknown</a>
 

 

