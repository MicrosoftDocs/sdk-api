---
UID: NF:wmp.IWMPEvents3.LibraryDisconnect
title: IWMPEvents3::LibraryDisconnect (wmp.h)
author: windows-sdk-content
description: The LibraryDisconnect event occurs when a library is no longer available.
old-location: wmp\iwmpevents3_iwmpevents3__librarydisconnect.htm
tech.root: WMP
ms.assetid: eb0f4d9f-23b7-4fe7-b45d-152a2f64af30
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: IWMPEvents3 interface [Windows Media Player],LibraryDisconnect method, IWMPEvents3.LibraryDisconnect, IWMPEvents3::LibraryDisconnect, IWMPEvents3LibraryDisconnect, LibraryDisconnect, LibraryDisconnect method [Windows Media Player], LibraryDisconnect method [Windows Media Player],IWMPEvents3 interface, wmp.iwmpevents3_iwmpevents3__librarydisconnect, wmp/IWMPEvents3::LibraryDisconnect
ms.topic: method
f1_keywords: 
 - "wmp/IWMPEvents3.LibraryDisconnect"
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
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
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




<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmpevents3">IWMPEvents3 Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/api/wmp/nn-wmp-iwmplibrary">IWMPLibrary Interface</a>



<a href="https://docs.microsoft.com/windows/desktop/WMP/-wmpocxevents-interface">_WMPOCXEvents Interface</a>
 

 

