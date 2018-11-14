---
UID: NF:uiribbon.IUICollectionChangedEvent.OnChanged
title: IUICollectionChangedEvent::OnChanged
author: windows-sdk-content
description: Called when an IUICollection changes.
old-location: windowsribbon\windowsribbon_iuicollectionchangedevent_onchanged.htm
tech.root: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollectionchangedevent\onchanged.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUICollectionChangedEvent interface [Windows Ribbon],OnChanged method, IUICollectionChangedEvent.OnChanged, IUICollectionChangedEvent::OnChanged, OnChanged, OnChanged method [Windows Ribbon], OnChanged method [Windows Ribbon],IUICollectionChangedEvent interface, scenicintent_IUICollectionChangedEvent_OnChanged, uiribbon/IUICollectionChangedEvent::OnChanged, windowsribbon.windowsribbon_iuicollectionchangedevent_onchanged
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: uiribbon.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: Mshtml.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Mshtml.dll
api_name:
 - IUICollectionChangedEvent.OnChanged
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- uiribbon.h
: 
- IUICollectionChangedEvent.OnChanged
: 
req.product: Windows UI
---

# IUICollectionChangedEvent::OnChanged


## -description


Called when an <a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a> changes.


## -parameters




### -param action [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/Dd371548(v=VS.85).aspx">UI_COLLECTIONCHANGE</a></b>

The <a href="https://msdn.microsoft.com/en-us/library/Dd371548(v=VS.85).aspx">action</a> performed on the 
					<a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a>.
				


### -param oldIndex [in]

Type: <b>UINT32</b>

Index of the old item on remove or replace; otherwise <a href="https://msdn.microsoft.com/en-us/library/Dd371551(v=VS.85).aspx">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param oldItem [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>*</b>

Pointer to the old item on remove or replace; otherwise <b>NULL</b>.
				


### -param newIndex [in]

Type: <b>UINT32</b>

Index of the new item on insert, add, or replace; otherwise <a href="https://msdn.microsoft.com/en-us/library/Dd371551(v=VS.85).aspx">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param newItem [in]

Type: <b><a href="https://msdn.microsoft.com/en-us/library/ms680509(v=VS.85).aspx">IUnknown</a>*</b>

Pointer to the new item on insert, add, or replace; otherwise <b>NULL</b>.
				


## -returns



Type: <b>HRESULT</b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The <b>IUICollectionChangedEvent::OnChanged</b> interface is implemented by the Ribbon host application 
				(the client connection sink) as a listener for collection changed 
				events that are fired by the Ribbon (the connectable object).
			




## -see-also




<a href="http://go.microsoft.com/fwlink/p/?linkid=132598">Events in COM and Connectable Objects</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd742704(v=VS.85).aspx">Gallery Sample</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371519(v=VS.85).aspx">IUICollection</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd371499(v=VS.85).aspx">IUICollectionChangedEvent</a>
 

 

