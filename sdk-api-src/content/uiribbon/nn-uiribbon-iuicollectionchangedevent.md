---
UID: NN:uiribbon.IUICollectionChangedEvent
title: IUICollectionChangedEvent (uiribbon.h)
description: The IUICollectionChangedEvent interface is implemented by the application and defines the method required to handle changes to a collection at run time.helpviewer_keywords: ["IUICollectionChangedEvent","IUICollectionChangedEvent interface [Windows Ribbon]","IUICollectionChangedEvent interface [Windows Ribbon]","described","scenicintent_IUICollectionChangedEvent","uiribbon/IUICollectionChangedEvent","windowsribbon.windowsribbon_iuicollectionchangedevent"]
old-location: windowsribbon\windowsribbon_iuicollectionchangedevent.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollectionchangedevent\iuicollectionchangedevent.htm
ms.date: 12/05/2018
ms.keywords: IUICollectionChangedEvent, IUICollectionChangedEvent interface [Windows Ribbon], IUICollectionChangedEvent interface [Windows Ribbon],described, scenicintent_IUICollectionChangedEvent, uiribbon/IUICollectionChangedEvent, windowsribbon.windowsribbon_iuicollectionchangedevent
f1_keywords:
- uiribbon/IUICollectionChangedEvent
dev_langs:
- c++
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
topic_type:
- APIRef
- kbSyntax
api_type:
- COM
api_location:
- Uiribbon.dll
api_name:
- IUICollectionChangedEvent
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IUICollectionChangedEvent interface


## -description


The <b>IUICollectionChangedEvent</b> interface is 
		implemented by the application and defines the method required to handle changes 
		to a collection at run time.


## -inheritance

The <b xmlns:loc="http://microsoft.com/wdcml/l10n">IUICollectionChangedEvent</b> interface inherits from the <a href="https://docs.microsoft.com/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IUICollectionChangedEvent</b> also has these types of members:
<ul>
<li><a href="https://docs.microsoft.com/">Methods</a></li>
</ul>

## -members

The <b>IUICollectionChangedEvent</b> interface has these methods.
<table class="members" id="memberListMethods">
<tr>
<th align="left" width="37%">Method</th>
<th align="left" width="63%">Description</th>
</tr>
<tr data="declared;">
<td align="left" width="37%">
<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged">OnChanged</a>
</td>
<td align="left" width="63%">
Called when an <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a> changes.

</td>
</tr>
</table> 


## -remarks



The Windows Ribbon framework incorporates the standard Component Object Model (COM)  client-server mechanism of <a href="https://msdn.microsoft.com/library/ms694379.aspx">connectable objects</a> to listen for and handle collection changed events at run time.

The Ribbon acts as the COM server connectable object that defines both incoming and outgoing notification interfaces for the client, which is the Ribbon host application. The incoming interfaces are implemented by the Ribbon. The  outgoing interfaces are implemented by the application in a dedicated object that is created by the application and  referred to as the client connection sink. This sink is used to establish a connection to the connectable object.

In addition to defining the incoming and outgoing interfaces, the Ribbon must also implement the <a href="https://msdn.microsoft.com/library/ms683857.aspx">IConnectionPointContainer</a> interface and  create at least one connection point object that implements the <a href="https://msdn.microsoft.com/library/ms694318.aspx">IConnectionPoint</a> interface and manages the connection with the client sink.

<div class="alert"><b>Note</b>  The client must query the connectable object for <a href="https://msdn.microsoft.com/library/ms683857.aspx">IConnectionPointContainer</a> to determine whether the object is connectable before the client attempts to create a sink object.</div>
<div> </div>
In the case of the Ribbon,  <b>IUICollectionChangedEvent</b> is the outgoing interface defined by the framework and implemented by the application. The Ribbon triggers the <a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nf-uiribbon-iuicollectionchangedevent-onchanged">IUICollectionChangedEvent::OnChanged</a> event in the client by sending an outgoing notification when a collection changes, for example, adding a Command to the Quick Access Toolbar (QAT).




## -see-also




<a href="https://msdn.microsoft.com/library/ms694379.aspx">Events in COM and Connectable Objects</a>



<a href="https://docs.microsoft.com/windows/desktop/windowsribbon/windowsribbon-gallerysample">Gallery Sample</a>



<a href="https://docs.microsoft.com/windows/desktop/api/uiribbon/nn-uiribbon-iuicollection">IUICollection</a>
 

 

