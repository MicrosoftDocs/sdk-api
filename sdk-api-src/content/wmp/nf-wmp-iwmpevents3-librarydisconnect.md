---
UID: NF:wmp.IWMPEvents3.LibraryDisconnect
title: IWMPEvents3::LibraryDisconnect
author: windows-sdk-content
description: The LibraryDisconnect event occurs when a library is no longer available.
old-location: wmp\iwmpevents3_iwmpevents3__librarydisconnect.htm
tech.root: WMP
ms.assetid: eb0f4d9f-23b7-4fe7-b45d-152a2f64af30
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: IWMPEvents3 interface [Windows Media Player],LibraryDisconnect method, IWMPEvents3.LibraryDisconnect, IWMPEvents3::LibraryDisconnect, IWMPEvents3LibraryDisconnect, LibraryDisconnect, LibraryDisconnect method [Windows Media Player], LibraryDisconnect method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__librarydisconnect, wmp/IWMPEvents3::LibraryDisconnect
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: wmp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Media Player 11.
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
req.lib: 
req.dll: Wmp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - wmp.dll
api_name:
 - IWMPEvents3.LibraryDisconnect
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- wmp.h
: 
- IWMPEvents3.LibraryDisconnect
: 
---

# IWMPEvents3::LibraryDisconnect


## -description



The <b>LibraryDisconnect</b> event occurs when a library is no longer available.




## -parameters




### -param pLibrary [in]

Pointer to the <b>IWMPLibrary</b> interface that represents the library that disconnected.


## -returns



This method does not return a value.




## -remarks



This event does not occur for the local library.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/add0ed43-d83f-4793-b1f6-ccad0f01854c">IWMPLibrary Interface</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

