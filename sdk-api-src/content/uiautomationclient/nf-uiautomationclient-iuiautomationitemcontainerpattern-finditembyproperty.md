---
UID: NF:uiautomationclient.IUIAutomationItemContainerPattern.FindItemByProperty
title: IUIAutomationItemContainerPattern::FindItemByProperty (uiautomationclient.h)
description: Retrieves an element within a containing element, based on a specified property value. (IUIAutomationItemContainerPattern.FindItemByProperty)
helpviewer_keywords: ["FindItemByProperty","FindItemByProperty method [Windows Accessibility]","FindItemByProperty method [Windows Accessibility]","IUIAutomationItemContainerPattern interface","IUIAutomationItemContainerPattern interface [Windows Accessibility]","FindItemByProperty method","IUIAutomationItemContainerPattern.FindItemByProperty","IUIAutomationItemContainerPattern::FindItemByProperty","uiauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty","uiauto_IUIAutomationItemContainerPattern_FindItemByProperty","uiautomationclient/IUIAutomationItemContainerPattern::FindItemByProperty","winauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty"]
old-location: winauto\uiauto_IUIAutomationItemContainerPattern_FindItemByProperty.htm
tech.root: WinAuto
ms.assetid: d27f07ae-2c88-4cde-99b8-0c8c987b95d3
ms.date: 12/05/2018
ms.keywords: FindItemByProperty, FindItemByProperty method [Windows Accessibility], FindItemByProperty method [Windows Accessibility],IUIAutomationItemContainerPattern interface, IUIAutomationItemContainerPattern interface [Windows Accessibility],FindItemByProperty method, IUIAutomationItemContainerPattern.FindItemByProperty, IUIAutomationItemContainerPattern::FindItemByProperty, uiauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty, uiauto_IUIAutomationItemContainerPattern_FindItemByProperty, uiautomationclient/IUIAutomationItemContainerPattern::FindItemByProperty, winauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty
req.header: uiautomationclient.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista, Windows XP with SP3 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008, Windows Server 2003 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: UIAutomationClient.idl
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
 - IUIAutomationItemContainerPattern::FindItemByProperty
 - uiautomationclient/IUIAutomationItemContainerPattern::FindItemByProperty
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationItemContainerPattern.FindItemByProperty
---

# IUIAutomationItemContainerPattern::FindItemByProperty


## -description

Retrieves an element within a containing element, based on a specified property value.

## -parameters

### -param pStartAfter [in]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>*</b>

A pointer to the element after which the search begins, or <b>NULL</b> to search all elements.

### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="/windows/desktop/WinAuto/uiauto-entry-propids">Property Identifiers</a>.

### -param value [in]

Type: <b><a href="/windows/desktop/api/oaidl/ns-oaidl-variant">VARIANT</a></b>

The property value.

### -param pFound [out, retval]

Type: <b><a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a>**</b>

Receives a pointer to the matching element.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

The provider may return an actual <a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationelement">IUIAutomationElement</a> interface or a placeholder if the matching element is virtualized.
        

This method returns E_INVALIDARG if the property requested is not one that the container supports searching over. It is expected that most containers will support Name property, and if appropriate for the container, AutomationId and IsSelected.
        

This method can be slow, because it may need to traverse multiple objects to find a matching one. When used in a loop to return multiple items, no specific order is defined so long as each item is returned only once (that is, the loop should terminate). This method is also item-centric, not UI-centric, so items with multiple UI representations need to be hit only once.
        

When the <i>propertyId</i> parameter is specified as 0 (zero), the provider is expected to return the next item after <i>pStartAfter</i>. If <i>pStartAfter</i> is specified as <b>NULL</b> with a <i>propertyId</i> of 0, the provider should return the first item in the container. When <i>propertyId</i> is specified as 0, the <i>value</i> parameter should be VT_EMPTY.

## -see-also

<a href="/windows/desktop/api/uiautomationclient/nn-uiautomationclient-iuiautomationitemcontainerpattern">IUIAutomationItemContainerPattern</a>



<a href="/windows/desktop/api/uiautomationclient/nf-uiautomationclient-iuiautomationvirtualizeditempattern-realize">Realize</a>



<b>Reference</b>
