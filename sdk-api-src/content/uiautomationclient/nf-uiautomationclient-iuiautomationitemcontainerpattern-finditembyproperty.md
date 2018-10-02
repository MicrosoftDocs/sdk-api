---
UID: NF:uiautomationclient.IUIAutomationItemContainerPattern.FindItemByProperty
title: IUIAutomationItemContainerPattern::FindItemByProperty
author: windows-sdk-content
description: Retrieves an element within a containing element, based on a specified property value.
old-location: winauto\uiauto_IUIAutomationItemContainerPattern_FindItemByProperty.htm
tech.root: WinAuto
ms.assetid: d27f07ae-2c88-4cde-99b8-0c8c987b95d3
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: FindItemByProperty, FindItemByProperty method [Windows Accessibility], FindItemByProperty method [Windows Accessibility],IUIAutomationItemContainerPattern interface, IUIAutomationItemContainerPattern interface [Windows Accessibility],FindItemByProperty method, IUIAutomationItemContainerPattern.FindItemByProperty, IUIAutomationItemContainerPattern::FindItemByProperty, uiauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty, uiauto_IUIAutomationItemContainerPattern_FindItemByProperty, uiautomationclient/IUIAutomationItemContainerPattern::FindItemByProperty, winauto.uiauto_IUIAutomationItemContainerPattern_FindItemByProperty
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationClient.h
api_name:
 - IUIAutomationItemContainerPattern.FindItemByProperty
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomationItemContainerPattern::FindItemByProperty


## -description


Retrieves an element within a containing element, based on a specified property value.


## -parameters




### -param pStartAfter

TBD


### -param propertyId [in]

Type: <b>PROPERTYID</b>

The property identifier. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param value [in]

Type: <b><a href="https://msdn.microsoft.com/e305240e-9e11-4006-98cc-26f4932d2118">VARIANT</a></b>

The property value.


### -param pFound

TBD




#### - pfound [out, retval]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>**</b>

Receives a pointer to the matching element.


#### - pstartAfter [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the element after which the search begins, or <b>NULL</b> to search all elements.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The provider may return an actual <a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a> interface or a placeholder if the matching element is virtualized.
        

This method returns E_INVALIDARG if the property requested is not one that the container supports searching over. It is expected that most containers will support Name property, and if appropriate for the container, AutomationId and IsSelected.
        

This method can be slow, because it may need to traverse multiple objects to find a matching one. When used in a loop to return multiple items, no specific order is defined so long as each item is returned only once (that is, the loop should terminate). This method is also item-centric, not UI-centric, so items with multiple UI representations need to be hit only once.
        

When the <i>propertyId</i> parameter is specified as 0 (zero), the provider is expected to return the next item after <i>pStartAfter</i>. If <i>pStartAfter</i> is specified as <b>NULL</b> with a <i>propertyId</i> of 0, the provider should return the first item in the container. When <i>propertyId</i> is specified as 0, the <i>value</i> parameter should be VT_EMPTY.
        




## -see-also




<a href="https://msdn.microsoft.com/87655c25-d666-4349-9750-566b60b37c56">IUIAutomationItemContainerPattern</a>



<a href="https://msdn.microsoft.com/33831b88-cce7-47f3-acd1-e6b74f5a93d2">Realize</a>



<b>Reference</b>
 

 

