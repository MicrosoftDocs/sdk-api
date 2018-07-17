---
UID: NF:mmc.INodeProperties.GetProperty
title: INodeProperties::GetProperty
author: windows-sdk-content
description: The GetProperty method retrieves text-only property values for a node. Your implementation of the INodeProperties::GetProperty method is called when an application based on the MMC 2.0 Automation Object Model retrieves the Node.Property property.
old-location: mmc\inodeproperties_getproperty.htm
old-project: mmc
ms.assetid: e891428a-c0a1-4451-aa69-c0a4a3d09078
ms.author: windowssdkdev
ms.date: 07/11/2018
ms.keywords: GetProperty, GetProperty method [MMC], GetProperty method [MMC],INodeProperties interface, INodeProperties interface [MMC],GetProperty method, INodeProperties.GetProperty, INodeProperties::GetProperty, _slate_inodeproperties_getproperty, mmc.inodeproperties_getproperty, mmc/INodeProperties::GetProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: mmc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: MMC_VIEW_TYPE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - INodeProperties.GetProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# INodeProperties::GetProperty


## -description


The 
<b>GetProperty</b> method retrieves text-only property values for a node. Your implementation of the <b>INodeProperties::GetProperty</b> method is called when an application based on the 
<a href="https://msdn.microsoft.com/eb7c92e7-d834-4736-bff4-74940c9bb194">MMC 2.0 Automation Object Model</a> retrieves the 
<a href="https://msdn.microsoft.com/edb52d1b-e422-4c94-9462-7dca2f15b231">Node.Property</a> property.


## -parameters




### -param pDataObject [in]

A pointer to the snap-in data object.


### -param szPropertyName [in]

The name of the property retrieved.


### -param pbstrProperty [out]

Text value for the property.


## -returns



The snap-in returns <b>S_OK</b> if it provides the property value when this method is called. If the snap-in returns <b>S_FALSE</b>, then the data object is queried for the property value.




## -remarks



The Extended View extension uses two properties: CCF_DESCRIPTION and CCF_HTML_DETAILS. As an alternative to supplying values for these properties using the data object to query the 
<a href="https://msdn.microsoft.com/eff5b42b-662a-49b0-bc32-9522e7c12704">CCF_DESCRIPTION</a> and 
<a href="https://msdn.microsoft.com/608826eb-e0ae-423c-98ed-4519d77e6d84">CCF_HTML_DETAILS</a> clipboard formats, a snap-in can use <b>INodeProperties::GetProperty</b> to return the property values to the Extended View. This alternative is beneficial in situations where a snap-in's data object does not provide the desired information.

In addition to providing CCF_DESCRIPTION and CCF_HTML_DETAILS property values, a snap-in can use 
INodeProperties to provide values for other text-based properties (for example, with a new view extension).

For more information and a code example for <b>INodeProperties::GetProperty</b>, see 
<a href="https://msdn.microsoft.com/e43f03c3-b0ef-43df-ac7a-9fa9aeea8b92">Using the Extended View Extension - Implementation Details</a>.




## -see-also




<a href="https://msdn.microsoft.com/eff5b42b-662a-49b0-bc32-9522e7c12704">CCF_DESCRIPTION</a>



<a href="https://msdn.microsoft.com/608826eb-e0ae-423c-98ed-4519d77e6d84">CCF_HTML_DETAILS</a>



<a href="https://msdn.microsoft.com/c504cb3f-8ec6-49fe-b0d3-05ea9cad61f4">Node</a>



<a href="https://msdn.microsoft.com/edb52d1b-e422-4c94-9462-7dca2f15b231">Node.Property</a>



<a href="https://msdn.microsoft.com/56fa12d4-a804-468f-9df5-7b0db786f79f">Using the Extended View Extension</a>



<a href="https://msdn.microsoft.com/e43f03c3-b0ef-43df-ac7a-9fa9aeea8b92">Using the Extended View Extension - Implementation Details</a>
 

 

