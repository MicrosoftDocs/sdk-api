---
UID: NF:uiautomationcore.IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent
title: IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent
author: windows-sdk-content
description: Raises a property-changed event.
old-location: winauto\uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent.htm
tech.root: WinAuto
ms.assetid: 84b8db1d-75ec-45b6-a4a5-c5d4bffe6978
ms.author: windowssdkdev
ms.date: 11/02/2018
ms.keywords: AddAutomationPropertyChangedEvent, AddAutomationPropertyChangedEvent method [Windows Accessibility], AddAutomationPropertyChangedEvent method [Windows Accessibility],IProxyProviderWinEventSink interface, IProxyProviderWinEventSink interface [Windows Accessibility],AddAutomationPropertyChangedEvent method, IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent, IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent, uiauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent, uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent, uiautomationcore/IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent, winauto.uiauto_IProxyProviderWinEventSink_AddAutomationPropertyChangedEvent
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiautomationcore.h
: 
- IProxyProviderWinEventSink.AddAutomationPropertyChangedEvent
: 
---

# IProxyProviderWinEventSink::AddAutomationPropertyChangedEvent


## -description


Raises a property-changed event.


## -parameters




### -param pProvider [in]

Type: <b><a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a>*</b>

A pointer to the provider for the element that will raise the event.


### -param id [in]

Type: <b>PROPERTYID</b>

The identifier of the property that is to be changed. For a list of property IDs, see <a href="https://msdn.microsoft.com/c05163ea-ba06-4005-9b80-661015b9d2ef">Property Identifiers</a>. 


### -param newValue [in]

Type: <b><a href="https://msdn.microsoft.com/774dfac8-e258-4266-b81e-072eb3961fb1">VARIANT</a></b>

The new value for the changed property.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -see-also




<a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a>
 

 

