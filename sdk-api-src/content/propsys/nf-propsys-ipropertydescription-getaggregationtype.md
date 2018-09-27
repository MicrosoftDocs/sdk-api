---
UID: NF:propsys.IPropertyDescription.GetAggregationType
title: IPropertyDescription::GetAggregationType
author: windows-sdk-content
description: Gets a value that describes how the property values are displayed when multiple items are selected in the UI.
old-location: properties\IPropertyDescription_GetAggregationType.htm
tech.root: properties
ms.assetid: d8507f19-1778-42b1-bd40-12fec45cd03e
ms.author: windowssdkdev
ms.date: 09/07/2018
ms.keywords: GetAggregationType, GetAggregationType method [Windows Properties], GetAggregationType method [Windows Properties],IPropertyDescription interface, IPropertyDescription interface [Windows Properties],GetAggregationType method, IPropertyDescription.GetAggregationType, IPropertyDescription::GetAggregationType, properties.IPropertyDescription_GetAggregationType, propsys/IPropertyDescription::GetAggregationType, shell.IPropertyDescription_GetAggregationType, shell_IPropertyDescription_GetAggregationType
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
 - IPropertyDescription.GetAggregationType
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IPropertyDescription::GetAggregationType


## -description


Gets a value that describes how the property values are displayed when multiple items are selected in the UI.


## -parameters




### -param paggtype [out]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Bb762522(v=VS.85).aspx">PROPDESC_AGGREGATION_TYPE</a>*</b>

When this method returns, contains a pointer to a value that indicates the aggregation type. See <a href="https://msdn.microsoft.com/en-us/library/Bb762522(v=VS.85).aspx">PROPDESC_AGGREGATION_TYPE</a>.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The information retrieved by this method comes from the <i>aggregationType</i> attribute of the <a href="https://msdn.microsoft.com/en-us/library/Bb773889(v=VS.85).aspx">typeInfo</a> element in the property's .propdesc file.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Bb761561(v=VS.85).aspx">IPropertyDescription</a>



<a href="https://msdn.microsoft.com/cac93c31-d90d-4116-b846-0cf593d1d56e">Property Description Schema</a>
 

 

