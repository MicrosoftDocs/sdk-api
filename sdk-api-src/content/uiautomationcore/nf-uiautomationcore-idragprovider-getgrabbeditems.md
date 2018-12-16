---
UID: NF:uiautomationcore.IDragProvider.GetGrabbedItems
title: IDragProvider::GetGrabbedItems
author: windows-sdk-content
description: Retrieves the collection of elements that are being dragged as part of a drag operation.
old-location: winauto\uiauto_idragprovider_getgrabbeditems.htm
tech.root: WinAuto
ms.assetid: B56F5975-279C-48C7-84C9-35BBBE222F6A
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: GetGrabbedItems, GetGrabbedItems method [Windows Accessibility], GetGrabbedItems method [Windows Accessibility],IDragProvider interface, IDragProvider interface [Windows Accessibility],GetGrabbedItems method, IDragProvider.GetGrabbedItems, IDragProvider::GetGrabbedItems, uiautomationcore/IDragProvider::GetGrabbedItems, winauto.uiauto_idragprovider_getgrabbeditems
ms.topic: method
req.header: uiautomationcore.h
req.include-header: UIAutomation.h
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps \| UWP apps]
req.target-min-winversvr: Windows Server 2012 [desktop apps \| UWP apps]
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
 - IDragProvider.GetGrabbedItems
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IDragProvider::GetGrabbedItems


## -description


Retrieves the collection of elements that are being dragged as part of a drag operation.  


## -parameters




### -param pRetVal [out, retval, optional]

An array of VT_UNKNOWN pointers to the <a href="https://msdn.microsoft.com/f0ec6185-acd0-4df7-88f4-fd00747f98bf">IRawElementProviderSimple</a> interfaces
				of the elements that are being dragged. This parameter is <b>NULL</b> if only a single item is being dragged. 


## -returns



If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



If the user is dragging multiple items, the items are represented by a single master element with an associated set of grabbed elements.  The master element raises the appropriate events, to avoid having a large set of duplicate events.  The client can call <b>GetGrabbedItems</b> to retrieve the full list of grabbed items.  The provider should allocate a <a href="https://go.microsoft.com/fwlink/p/?linkid=180754">SAFEARRAY</a> of appropriate length and add the Component Object Model (COM) pointers of the elements that are part of the drag operation.  




## -see-also




<a href="https://msdn.microsoft.com/FAC4A56D-17BC-42E6-A03E-EE45D717DE37">IDragProvider</a>
 

 

