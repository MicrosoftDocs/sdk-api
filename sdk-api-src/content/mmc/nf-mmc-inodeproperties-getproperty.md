---
UID: NF:mmc.INodeProperties.GetProperty
title: INodeProperties::GetProperty (mmc.h)
description: The GetProperty method retrieves text-only property values for a node. Your implementation of the INodeProperties::GetProperty method is called when an application based on the MMC 2.0 Automation Object Model retrieves the Node.Property property.
helpviewer_keywords: ["GetProperty","GetProperty method [MMC]","GetProperty method [MMC]","INodeProperties interface","INodeProperties interface [MMC]","GetProperty method","INodeProperties.GetProperty","INodeProperties::GetProperty","_slate_inodeproperties_getproperty","mmc.inodeproperties_getproperty","mmc/INodeProperties::GetProperty"]
old-location: mmc\inodeproperties_getproperty.htm
tech.root: mmc
ms.assetid: e891428a-c0a1-4451-aa69-c0a4a3d09078
ms.date: 12/05/2018
ms.keywords: GetProperty, GetProperty method [MMC], GetProperty method [MMC],INodeProperties interface, INodeProperties interface [MMC],GetProperty method, INodeProperties.GetProperty, INodeProperties::GetProperty, _slate_inodeproperties_getproperty, mmc.inodeproperties_getproperty, mmc/INodeProperties::GetProperty
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
req.lib: 
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - INodeProperties::GetProperty
 - mmc/INodeProperties::GetProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mmc.h
api_name:
 - INodeProperties.GetProperty
---

# INodeProperties::GetProperty


## -description

The 
<b>GetProperty</b> method retrieves text-only property values for a node. Your implementation of the <b>INodeProperties::GetProperty</b> method is called when an application based on the 
<a href="/previous-versions/windows/desktop/mmc/mmc-2-0-automation-object-model">MMC 2.0 Automation Object Model</a> retrieves the 
<a href="/previous-versions/windows/desktop/mmc/node-property">Node.Property</a> property.

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
<a href="/previous-versions/windows/desktop/mmc/ccf-description">CCF_DESCRIPTION</a> and 
<a href="/previous-versions/windows/desktop/mmc/ccf-html-details">CCF_HTML_DETAILS</a> clipboard formats, a snap-in can use <b>INodeProperties::GetProperty</b> to return the property values to the Extended View. This alternative is beneficial in situations where a snap-in's data object does not provide the desired information.

In addition to providing CCF_DESCRIPTION and CCF_HTML_DETAILS property values, a snap-in can use 
INodeProperties to provide values for other text-based properties (for example, with a new view extension).

For more information and a code example for <b>INodeProperties::GetProperty</b>, see 
<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension-implementation-details">Using the Extended View Extension - Implementation Details</a>.

## -see-also

<a href="/previous-versions/windows/desktop/mmc/ccf-description">CCF_DESCRIPTION</a>



<a href="/previous-versions/windows/desktop/mmc/ccf-html-details">CCF_HTML_DETAILS</a>



<a href="/previous-versions/windows/desktop/mmc/node-object">Node</a>



<a href="/previous-versions/windows/desktop/mmc/node-property">Node.Property</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension">Using the Extended View Extension</a>



<a href="/previous-versions/windows/desktop/mmc/using-the-extended-view-extension-implementation-details">Using the Extended View Extension - Implementation Details</a>