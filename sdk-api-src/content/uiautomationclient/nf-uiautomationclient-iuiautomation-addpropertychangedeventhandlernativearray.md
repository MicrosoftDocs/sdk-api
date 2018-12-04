---
UID: NF:uiautomationclient.IUIAutomation.AddPropertyChangedEventHandlerNativeArray
title: IUIAutomation::AddPropertyChangedEventHandlerNativeArray
author: windows-sdk-content
description: Registers a method that handles property-changed events.
old-location: winauto\uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray.htm
tech.root: WinAuto
ms.assetid: 0d3cf5c3-5d0e-4214-a9fc-8b0132ad9b77
ms.author: windowssdkdev
ms.date: 11/16/2018
ms.keywords: AddPropertyChangedEventHandlerNativeArray, AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility], AddPropertyChangedEventHandlerNativeArray method [Windows Accessibility],IUIAutomation interface, IUIAutomation interface [Windows Accessibility],AddPropertyChangedEventHandlerNativeArray method, IUIAutomation.AddPropertyChangedEventHandlerNativeArray, IUIAutomation::AddPropertyChangedEventHandlerNativeArray, uiauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray, uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray, uiautomationclient/IUIAutomation::AddPropertyChangedEventHandlerNativeArray, winauto.uiauto_IUIAutomation_AddPropertyChangedEventHandlerNativeArray
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
 - IUIAutomation.AddPropertyChangedEventHandlerNativeArray
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IUIAutomation::AddPropertyChangedEventHandlerNativeArray


## -description


Registers a method that handles property-changed events. 
<div class="alert"><b>Note</b>  Before implementing an event handler, you should be familiar with the threading issues described in <a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>.</div><div> </div>

## -parameters




### -param element [in]

Type: <b><a href="https://msdn.microsoft.com/9e1f87b1-a204-4ca9-acf2-a40277012207">IUIAutomationElement</a>*</b>

A pointer to the UI Automation element associated with the event handler.


### -param arg2 [in]

Type: <b><a href="https://msdn.microsoft.com/eb9e05b3-bcfa-4fed-9cc9-6ea8a778618e">TreeScope</a></b>

The scope of events to be handled; that is, whether they are on the element itself, or on its ancestors and children.


### -param cacheRequest [in]

Type: <b><a href="https://msdn.microsoft.com/8e5d7f6e-c4c7-4bb9-ba33-959e098ecd41">IUIAutomationCacheRequest</a>*</b>

A pointer to a cache request, or <b>NULL</b> if no caching is wanted.


### -param handler [in]

Type: <b><a href="https://msdn.microsoft.com/e89d1600-35f0-4baa-a32a-265a7ef82679">IUIAutomationPropertyChangedEventHandler</a>*</b>

A pointer to the object that handles the event.


### -param propertyArray [in]

Type: <b>PROPERTYID*</b>

A pointer to the identifiers of the UI Automation properties of interest.  For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>.


### -param propertyCount [in]

Type: <b>int</b>

The number of property identifiers in <i>propertyArray</i>.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The UI item specified by <i>element</i> might not support the properties specified by the <i>propertyArray</i> parameter. 

This method serves the same purpose as <a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">IUIAutomation::AddPropertyChangedEventHandler</a>, but takes a normal array of property identifiers instead of a SAFEARRAY. 
			

A UI Automation client should not use multiple threads to add or remove event handlers. Unexpected behavior can result if one event handler is being added or removed while another is being added or removed in the same client process.




## -see-also




<a href="https://msdn.microsoft.com/2623a48e-8818-486c-9bde-b218cde49189">AddPropertyChangedEventHandler</a>



<a href="https://msdn.microsoft.com/948b3bb9-75a9-4197-9680-e6fe7bb86feb">Caching UI Automation Properties and Control Patterns</a>



<b>Conceptual</b>



<a href="https://msdn.microsoft.com/46b31ab6-39aa-4df8-a421-6369c32a9605">IUIAutomation</a>



<b>Reference</b>



<a href="https://msdn.microsoft.com/3bf6d15a-2aaf-4f94-a852-f9cbd25cd496">RemoveAllEventHandlers</a>



<a href="https://msdn.microsoft.com/d8f7600f-a33e-4f30-ae8e-423f9c71edbe">RemovePropertyChangedEventHandler</a>



<a href="https://msdn.microsoft.com/7019ecb8-6123-4e00-926c-6725d7e71385">Subscribing to UI Automation Events</a>



<a href="https://msdn.microsoft.com/0772969a-da55-488e-8b21-7368434df8a9">Understanding Threading Issues</a>
 

 

