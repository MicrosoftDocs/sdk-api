---
UID: NN:uiribbon.IUICollectionChangedEvent
title: IUICollectionChangedEvent (uiribbon.h)
description: The IUICollectionChangedEvent interface is implemented by the application and defines the method required to handle changes to a collection at run time.
helpviewer_keywords: ["IUICollectionChangedEvent","IUICollectionChangedEvent interface [Windows Ribbon]","IUICollectionChangedEvent interface [Windows Ribbon]","described","scenicintent_IUICollectionChangedEvent","uiribbon/IUICollectionChangedEvent","windowsribbon.windowsribbon_iuicollectionchangedevent"]
old-location: windowsribbon\windowsribbon_iuicollectionchangedevent.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollectionchangedevent\iuicollectionchangedevent.htm
ms.date: 12/05/2018
ms.keywords: IUICollectionChangedEvent, IUICollectionChangedEvent interface [Windows Ribbon], IUICollectionChangedEvent interface [Windows Ribbon],described, scenicintent_IUICollectionChangedEvent, uiribbon/IUICollectionChangedEvent, windowsribbon.windowsribbon_iuicollectionchangedevent
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7, Windows Vista with SP2 and Platform Update for Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2, Windows Server 2008 with SP2 and Platform Update for Windows Server 2008 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Uiribbon.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: 
req.dll: Uiribbon.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IUICollectionChangedEvent
 - uiribbon/IUICollectionChangedEvent
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Uiribbon.dll
api_name:
 - IUICollectionChangedEvent
---

# IUICollectionChangedEvent interface


## -description

The <b>IUICollectionChangedEvent</b> interface is 
		implemented by the application and defines the method required to handle changes 
		to a collection at run time.

## -inheritance

The <b>IUICollectionChangedEvent</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUICollectionChangedEvent</b> also has these types of members:

## -remarks

The Windows Ribbon framework incorporates the standard Component Object Model (COM)  client-server mechanism of <a href="/windows/win32/com/events-in-com-and-connectable-objects">connectable objects</a> to listen for and handle collection changed events at run time.

The Ribbon acts as the COM server connectable object that defines both incoming and outgoing notification interfaces for the client, which is the Ribbon host application. The incoming interfaces are implemented by the Ribbon. The  outgoing interfaces are implemented by the application in a dedicated object that is created by the application and  referred to as the client connection sink. This sink is used to establish a connection to the connectable object.

In addition to defining the incoming and outgoing interfaces, the Ribbon must also implement the <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> interface and  create at least one connection point object that implements the <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpoint">IConnectionPoint</a> interface and manages the connection with the client sink.

<div class="alert"><b>Note</b>  The client must query the connectable object for <a href="/windows/win32/api/ocidl/nn-ocidl-iconnectionpointcontainer">IConnectionPointContainer</a> to determine whether the object is connectable before the client attempts to create a sink object.</div>
<div> </div>
In the case of the Ribbon,  <b>IUICollectionChangedEvent</b> is the outgoing interface defined by the framework and implemented by the application. The Ribbon triggers the <a href="/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged">IUICollectionChangedEvent::OnChanged</a> event in the client by sending an outgoing notification when a collection changes, for example, adding a Command to the Quick Access Toolbar (QAT).

## -see-also

<a href="/windows/win32/com/events-in-com-and-connectable-objects">Events in COM and Connectable Objects</a>



<a href="/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>
