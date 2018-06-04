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

# IItemContainerProvider::FindItemByProperty


## -description


Retrieves an element within a containing element, based on a specified property value.


## -parameters




### -param pStartAfter [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

The UI Automation provider of the element after which the search begins, or <b>NULL</b> to search all elements.


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/library/windows/hardware/mt138335">VARIANT</a></b>

The value of the property.


### -param pFound [out]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>**</b>

Receives a pointer to the UI Automation provider of the element.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



For virtual lists, the element returned may be a placeholder. <a href="https://msdn.microsoft.com/ec69f0d2-a643-4f1b-892a-0d90f79afe72">IVirtualizedItemProvider::Realize</a> can then be used to make the item fully available.

The method returns E_INVALIDARG if searching by the specified property is not supported. Most containers should support <a href="uiauto_automation_element_propids.htm">UIA_NamePropertyId</a> and, if appropriate, <a href="uiauto_automation_element_propids.htm">UIA_AutomationIdPropertyId</a> and <a href="uiauto_control_pattern_propids.htm">UIA_SelectionItemIsSelectedPropertyId</a>.

If <i>propertyId</i> is 0, all items are a match. This value can be  used
with <i>pStartAfter</i> equalling <b>NULL</b> to get the first item, and then to get successive
items. In this case, <i>value</i> should be VT_EMPTY.




## -see-also




<b>Conceptual</b>



<a href="https://msdn.microsoft.com/403436f5-7540-455b-965e-e2e3b64ef7e0">IItemContainerProvider</a>



<a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>



<b>Reference</b>
 

 

