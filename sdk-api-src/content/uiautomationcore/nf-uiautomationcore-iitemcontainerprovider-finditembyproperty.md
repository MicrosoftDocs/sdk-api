---
UID: NF:uiautomationcore.IItemContainerProvider.FindItemByProperty
title: IItemContainerProvider::FindItemByProperty
author: windows-sdk-content
description: Retrieves an element within a containing element, based on a specified property value.
old-location: winauto\uiauto_IItemContainerProvider_FindItemByProperty.htm
old-project: WinAuto
ms.assetid: f2873bbb-5bb4-4eaa-b0bd-60061fc06f53
ms.author: windowssdkdev
ms.date: 04/16/2018
ms.keywords: FindItemByProperty, FindItemByProperty method [Windows Accessibility], FindItemByProperty method [Windows Accessibility],IItemContainerProvider interface, IItemContainerProvider interface [Windows Accessibility],FindItemByProperty method, IItemContainerProvider.FindItemByProperty, IItemContainerProvider::FindItemByProperty, uiauto.uiauto_IItemContainerProvider_FindItemByProperty, uiauto_IItemContainerProvider_FindItemByProperty, uiautomationcore/IItemContainerProvider::FindItemByProperty, winauto.uiauto_IItemContainerProvider_FindItemByProperty
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: 
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Uiautomationcore.dll
api_name:
-	IItemContainerProvider.FindItemByProperty
product: Windows
targetos: Windows
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
req.product: Windows XP with SP1 and later
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
 

 

