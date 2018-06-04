---
UID: The unique id of the API.
title: The title of the API.
author: Authoring type of the API(ie windows-driver-content)
description: Description of API
old-location: 
old-project: 
ms.assetid: The MSDN ID of the API
ms.author: The Author of the API
ms.date: The date of API publishing
ms.keywords: 
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: The topic type of the API (ie enum)
req.header: The main header of the API
req.include-header: The included headers of the API
req.target-type: 
req.target-min-winverclnt: 
req.target-min-winversvr: 
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
---

# IProxyProviderWinEventHandler::RespondToWinEvent


## -description


Handles a WinEvent.


## -parameters




### -param idWinEvent [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">DWORD</a></b>

The identifier of the incoming <a href="https://msdn.microsoft.com/ba97b00b-4a4c-4889-ae9c-8e92eb742849">WinEvent</a>. For a list of WinEvent IDs, see <a href="https://msdn.microsoft.com/library/windows/hardware/ff597567">Event Constants</a>.


### -param hwnd [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HWND</a></b>

The handle of the window for which the WinEvent was fired. This should also be the window for which the proxy was created.


### -param idObject [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The object identifier (OBJID_*) of the accessible object associated with the event. For a list of object identifiers, see <a href="https://msdn.microsoft.com/dc1603f8-29e5-4acd-817a-c6957feaff6c">Object Identifiers</a>.


### -param idChild [in]

Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">LONG</a></b>

The child identifier of the element associated with the event, or <b>CHILDID_SELF</b> if the element is not a child.


### -param pSink [in]

Type: <b><a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a>*</b>

A pointer to the <a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a> interface provided by the UI Automation core. Any event that the proxy needs to raise in response to the WinEvent being handled should be added to the sink.


## -returns



Type: <b><a href="https://msdn.microsoft.com/4553cafc-450e-4493-a4d4-cb6e2f274d46">HRESULT</a></b>

If this method succeeds, it returns <b xmlns:loc="http://microsoft.com/wdcml/l10n">S_OK</b>. Otherwise, it returns an <b xmlns:loc="http://microsoft.com/wdcml/l10n">HRESULT</b> error code.




## -remarks



The provider should review the event data. If the provider needs to raise a UI Automation event in response, the data for that event should be added to the <i>pSink</i> event sink.




## -see-also




<a href="https://msdn.microsoft.com/3105ce04-fc99-494a-8db2-1a221af61c0a">IProxyProviderWinEventHandler</a>



<a href="https://msdn.microsoft.com/55489e34-ab23-4c65-9d6f-e2ff39bca74c">IProxyProviderWinEventSink</a>



<b>Reference</b>
 

 

