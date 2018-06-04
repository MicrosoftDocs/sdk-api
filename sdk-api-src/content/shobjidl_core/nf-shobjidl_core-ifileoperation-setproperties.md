---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IFileOperation::SetProperties


## -description


Declares a set of properties and values to be set on an item or items.


## -parameters




### -param pproparray [in]

Type: <b><a href="https://msdn.microsoft.com/c7de40d0-9fe6-4c4b-ba17-c4648501ce0a">IPropertyChangeArray</a>*</b>

Pointer to an <a href="https://msdn.microsoft.com/c7de40d0-9fe6-4c4b-ba17-c4648501ce0a">IPropertyChangeArray</a>, which accesses a collection of <a href="https://msdn.microsoft.com/7bdc31d8-ba03-4010-8aa1-89701ebbf8cd">IPropertyChange</a> objects that specify the properties to be set and their new values.


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



This method does not set the new property values, it merely declares them. To set property values on an item or a group of items, you must make at least the sequence of calls detailed here:

                

<ol>
<li>Call <b>IFileOperation::SetProperties</b> to declare the specific properties to be set and their new values.</li>
<li>Call <a href="https://msdn.microsoft.com/35330c7c-29fc-4337-a538-863925398b0d">IFileOperation::ApplyPropertiesToItem</a> or <a href="https://msdn.microsoft.com/d24aa63e-99ef-470c-9723-e561ee0a56bc">IFileOperation::ApplyPropertiesToItems</a> to declare the item or items whose properties are to be set.</li>
<li>Call <a href="https://msdn.microsoft.com/eceb5f0a-ad9a-4b7a-9656-c10e0420a96a">IFileOperation::PerformOperations</a> to apply the properties to the item or items.</li>
</ol>


