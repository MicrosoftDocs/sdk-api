---
UID: NF:uiribbon.IUICollectionChangedEvent.OnChanged
title: IUICollectionChangedEvent::OnChanged
author: windows-sdk-content
description: Called when an IUICollection changes.
old-location: windowsribbon\windowsribbon_iuicollectionchangedevent_onchanged.htm
old-project: windowsribbon
ms.assetid: VS|scenicintent|~\scenicintent\reference\ifaces\iuicollectionchangedevent\onchanged.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: IUICollectionChangedEvent interface [Windows Ribbon],OnChanged method, IUICollectionChangedEvent.OnChanged, IUICollectionChangedEvent::OnChanged, OnChanged, OnChanged method [Windows Ribbon], OnChanged method [Windows Ribbon],IUICollectionChangedEvent interface, scenicintent_IUICollectionChangedEvent_OnChanged, uiribbon/IUICollectionChangedEvent::OnChanged, windowsribbon.windowsribbon_iuicollectionchangedevent_onchanged
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: UI_VIEWVERB
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
req.lib: 
req.dll: Mshtml.dll
req.irql: 
req.product: Windows UI
---

# IUICollectionChangedEvent::OnChanged


## -description


Called when an <a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a> changes.


## -parameters




### -param action [in]

Type: <b><a href="https://msdn.microsoft.com/8edb3772-04c6-45ac-8ccf-2b8ddd37db6d">UI_COLLECTIONCHANGE</a></b>

The <a href="https://msdn.microsoft.com/library/windows/hardware/mt270124">action</a> performed on the 
					<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>.
				


### -param oldIndex [in]

Type: <b>UINT32</b>

Index of the old item on remove or replace; otherwise <a href="https://msdn.microsoft.com/0524c712-c968-4a2c-955e-c92f21f2b1da">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param oldItem [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>

Pointer to the old item on remove or replace; otherwise <b>NULL</b>.
				


### -param newIndex [in]

Type: <b>UINT32</b>

Index of the new item on insert, add, or replace; otherwise <a href="https://msdn.microsoft.com/0524c712-c968-4a2c-955e-c92f21f2b1da">UI_COLLECTION_INVALIDINDEX</a>.
				


### -param newItem [in]

Type: <b><a href="_com_iunknown">IUnknown</a>*</b>

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



<a href="https://msdn.microsoft.com/1a462f4e-e75a-40cf-9c52-0bad0a645d57">Gallery Sample</a>



<a href="https://msdn.microsoft.com/c239a724-9d7e-4204-933a-8e10581b4ecc">IUICollection</a>



<a href="https://msdn.microsoft.com/f2342459-af53-4442-8280-27ad96e5868e">IUICollectionChangedEvent</a>
 

 

