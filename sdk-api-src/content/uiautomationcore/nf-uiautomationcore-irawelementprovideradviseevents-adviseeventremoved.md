---
UID: NF:uiautomationcore.IRawElementProviderAdviseEvents.AdviseEventRemoved
title: IRawElementProviderAdviseEvents::AdviseEventRemoved (uiautomationcore.h)
description: Notifies the Microsoft UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event.
helpviewer_keywords: ["AdviseEventRemoved","AdviseEventRemoved method [Windows Accessibility]","AdviseEventRemoved method [Windows Accessibility]","IRawElementProviderAdviseEvents interface","IRawElementProviderAdviseEvents interface [Windows Accessibility]","AdviseEventRemoved method","IRawElementProviderAdviseEvents.AdviseEventRemoved","IRawElementProviderAdviseEvents::AdviseEventRemoved","uiauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved","uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved","uiautomationcore/IRawElementProviderAdviseEvents::AdviseEventRemoved","winauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved"]
old-location: winauto\uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved.htm
tech.root: WinAuto
ms.assetid: 42c9aeeb-dc08-4c13-ae86-2c0fb93e5c17
ms.date: 12/05/2018
ms.keywords: AdviseEventRemoved, AdviseEventRemoved method [Windows Accessibility], AdviseEventRemoved method [Windows Accessibility],IRawElementProviderAdviseEvents interface, IRawElementProviderAdviseEvents interface [Windows Accessibility],AdviseEventRemoved method, IRawElementProviderAdviseEvents.AdviseEventRemoved, IRawElementProviderAdviseEvents::AdviseEventRemoved, uiauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved, uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved, uiautomationcore/IRawElementProviderAdviseEvents::AdviseEventRemoved, winauto.uiauto_IRawElementProviderAdviseEvents_AdviseEventRemoved
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2003 [desktop apps \| UWP apps]
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IRawElementProviderAdviseEvents::AdviseEventRemoved
 - uiautomationcore/IRawElementProviderAdviseEvents::AdviseEventRemoved
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - UIAutomationCore.h
api_name:
 - IRawElementProviderAdviseEvents.AdviseEventRemoved
---

# IRawElementProviderAdviseEvents::AdviseEventRemoved


## -description

Notifies the Microsoft UI Automation provider when a UI Automation client stops listening for a specific event, including a property-changed event.

## -parameters

### -param eventId [in]

Type: <b>EVENTID</b>

The identifier of the event being removed. For a list of event IDs, see <a href="/windows/desktop/WinAuto/uiauto-event-ids">Event Identifiers</a>.

### -param propertyIDs [in]

Type: <b><a href="/windows/win32/api/oaidl/ns-oaidl-safearray">SAFEARRAY</a>*</b>

A pointer to the identifiers of the properties being removed, or <b>NULL</b> if the event listener being removed is not listening for property events.

## -returns

Type: <b><a href="/windows/desktop/WinProg/windows-data-types">HRESULT</a></b>

If this method succeeds, it returns <b>S_OK</b>. Otherwise, it returns an <b>HRESULT</b> error code.

## -remarks

This method enables the provider to reduce overhead by raising only events that are being listened for.

It is important for UI Automation providers to treat the <b>IRawElementProviderAdviseEvents::AdviseEventRemoved</b> like the <a href="/windows/desktop/api/unknwn/nf-unknwn-iunknown-release">Release</a> method of the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. As long as <a href="/windows/desktop/api/uiautomationcore/nf-uiautomationcore-irawelementprovideradviseevents-adviseeventadded">AdviseEventAdded</a> has been called more times than <b>AdviseEventRemoved</b> for a specific event or property, the provider should continue to raise corresponding events, because some clients are still listening. Alternatively, UI Automation providers can use the <a href="/windows/desktop/api/uiautomationcoreapi/nf-uiautomationcoreapi-uiaclientsarelistening">UiaClientsAreListening</a> function to determine if at least one client is listening and, if so, raise all appropriate events.

## -see-also

<a href="/windows/desktop/WinAuto/uiauto-workingwithsafearrays">Best Practices for Using Safe Arrays</a>



<b>Conceptual</b>



<a href="/windows/desktop/api/uiautomationcore/nn-uiautomationcore-irawelementprovideradviseevents">IRawElementProviderAdviseEvents</a>



<b>Reference</b>