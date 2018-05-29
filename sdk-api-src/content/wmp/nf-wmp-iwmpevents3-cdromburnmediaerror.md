---
UID: NF:wmp.IWMPEvents3.CdromBurnMediaError
title: IWMPEvents3::CdromBurnMediaError
author: windows-sdk-content
description: The CdromBurnMediaError event occurs when an error happens while burning an individual media item to a CD.
old-location: wmp\iwmpevents3_iwmpevents3__cdromburnmediaerror.htm
old-project: WMP
ms.assetid: 4bad9de2-8899-4149-965c-7835bd854f6f
ms.author: windowssdkdev
ms.date: 05/04/2018
ms.keywords: CdromBurnMediaError, CdromBurnMediaError method [Windows Media Player], CdromBurnMediaError method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromBurnMediaError method, IWMPEvents3.CdromBurnMediaError, IWMPEvents3::CdromBurnMediaError, IWMPEvents3CdromBurnMediaError, wmp.iwmpevents3_iwmpevents3__cdromburnmediaerror, wmp/IWMPEvents3::CdromBurnMediaError
ms.prod: windows
ms.technology: windows-sdk
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
-	IWMPEvents3.CdromBurnMediaError
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents3::CdromBurnMediaError


## -description



The <b>CdromBurnMediaError</b> event occurs when an error happens while burning an individual media item to a CD.




## -parameters




### -param pCdromBurn [in]

Pointer to the <b>IWMPCdromBurn</b> interface that represents the burning operation that raised the error.


### -param pMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item that raised the error. Call <b>QueryInterface</b> through this pointer to retrieve a pointer to <b>IWMPMedia</b>.


## -returns



This method does not return a value.




## -remarks



To capture generic errors, handle the <b>CdromBurnError</b> event.

You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/ea1ded30-4fca-4208-9fc2-f93c169f33b6">IWMPEvents3::CdromBurnError</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

