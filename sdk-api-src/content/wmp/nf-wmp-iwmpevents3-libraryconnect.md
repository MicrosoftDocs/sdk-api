---
UID: NF:wmp.IWMPEvents3.LibraryConnect
title: IWMPEvents3::LibraryConnect method
author: windows-driver-content
description: The LibraryConnect event occurs when a library becomes available.
old-location: wmp\iwmpevents3_iwmpevents3__libraryconnect.htm
old-project: WMP
ms.assetid: b9e1feb7-c894-4f37-9756-378740637f6e
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: IWMPEvents3, IWMPEvents3 interface [Windows Media Player], LibraryConnect method, IWMPEvents3::LibraryConnect, IWMPEvents3LibraryConnect, LibraryConnect method [Windows Media Player], LibraryConnect method [Windows Media Player], IWMPEvents3 interface, LibraryConnect,IWMPEvents3.LibraryConnect, wmp.iwmpevents3_iwmpevents3__libraryconnect, wmp/IWMPEvents3::LibraryConnect
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
req.typenames: WMPSyncState
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	wmp.dll
api_name:
-	IWMPEvents3.LibraryConnect
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents3::LibraryConnect method


## -description



The <b>LibraryConnect</b> event occurs when a library becomes available.




## -parameters




### -param pLibrary [in]

Pointer to the <b>IWMPLibrary</b> interface that represents the library that connected.


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
 

 

