---
UID: NF:uiautomationcore.IItemContainerProvider.FindItemByProperty
title: IItemContainerProvider::FindItemByProperty (uiautomationcore.h)
description: Retrieves an element within a containing element, based on a specified property value. (IItemContainerProvider.FindItemByProperty)
helpviewer_keywords: ["FindItemByProperty","FindItemByProperty method [Windows Accessibility]","FindItemByProperty method [Windows Accessibility]","IItemContainerProvider interface","IItemContainerProvider interface [Windows Accessibility]","FindItemByProperty method","IItemContainerProvider.FindItemByProperty","IItemContainerProvider::FindItemByProperty","uiauto.uiauto_IItemContainerProvider_FindItemByProperty","uiauto_IItemContainerProvider_FindItemByProperty","uiautomationcore/IItemContainerProvider::FindItemByProperty","winauto.uiauto_IItemContainerProvider_FindItemByProperty"]
old-location: winauto\uiauto_IItemContainerProvider_FindItemByProperty.htm
tech.root: WinAuto
ms.assetid: f2873bbb-5bb4-4eaa-b0bd-60061fc06f53
ms.date: 12/05/2018
ms.keywords: FindItemByProperty, FindItemByProperty method [Windows Accessibility], FindItemByProperty method [Windows Accessibility],IItemContainerProvider interface, IItemContainerProvider interface [Windows Accessibility],FindItemByProperty method, IItemContainerProvider.FindItemByProperty, IItemContainerProvider::FindItemByProperty, uiauto.uiauto_IItemContainerProvider_FindItemByProperty, uiauto_IItemContainerProvider_FindItemByProperty, uiautomationcore/IItemContainerProvider::FindItemByProperty, winauto.uiauto_IItemContainerProvider_FindItemByProperty
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps \| UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationCore.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiautomationcore.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IItemContainerProvider::FindItemByProperty
 - uiautomationcore/IItemContainerProvider::FindItemByProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiautomationcore.dll
api_name:
 - IItemContainerProvider.FindItemByProperty
---

# IItemContainerProvider::FindItemByProperty


## -description

Retrieves an element within a containing element, based on a specified property value.

## -parameters

### -param pStartAfter [in]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>*</b>

The UI Automation provider of the element after which the search begins, or <b>NULL</b> to search all elements.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param value [in]

Type: <b><a href="/windows/desktop/WinAuto/variant-structure">VARIANT</a></b>

The value of the property.

### -param pFound [out]

Type: <b><a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovidersimple">IRawElementProviderSimple</a>**</b>

Receives a pointer to the UI Automation provider of the element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

For virtual lists, the element returned may be a placeholder. <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-ivirtualizeditemprovider-realize">IVirtualizedItemProvider::Realize</a> can then be used to make the item fully available.

The method returns E_INVALIDARG if searching by the specified property is not supported. Most containers should support <a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">UIA_NamePropertyId</a> and, if appropriate, <a href="/windows/desktop/WinAuto/uiauto-automation-element-propids">UIA_AutomationIdPropertyId</a> and <a href="/windows/desktop/WinAuto/uiauto-control-pattern-propids">UIA_SelectionItemIsSelectedPropertyId</a>.

If <i>propertyId</i> is 0, all items are a match. This value can be  used
with <i>pStartAfter</i> equalling <b>NULL</b> to get the first item, and then to get successive
items. In this case, <i>value</i> should be VT_EMPTY.

## -see-also

<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-iitemcontainerprovider">IItemContainerProvider</a>



<a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>



<b>Reference</b>
