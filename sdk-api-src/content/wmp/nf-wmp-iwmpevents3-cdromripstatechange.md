---
UID: NF:wmp.IWMPEvents3.CdromRipStateChange
title: IWMPEvents3::CdromRipStateChange method
author: windows-driver-content
description: The CdromRipStateChange event occurs when a CD ripping operation changes state.
old-location: wmp\iwmpevents3_iwmpevents3__cdromripstatechange.htm
old-project: WMP
ms.assetid: 08445295-4fed-412f-84ce-eaf337758472
ms.author: windowsdriverdev
ms.date: 4/2/2018
ms.keywords: CdromRipStateChange method [Windows Media Player], CdromRipStateChange method [Windows Media Player], IWMPEvents3 interface, CdromRipStateChange,IWMPEvents3.CdromRipStateChange, IWMPEvents3, IWMPEvents3 interface [Windows Media Player], CdromRipStateChange method, IWMPEvents3::CdromRipStateChange, IWMPEvents3CdromRipStateChange, wmp.iwmpevents3_iwmpevents3__cdromripstatechange, wmp/IWMPEvents3::CdromRipStateChange
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
-	IWMPEvents3.CdromRipStateChange
product: Windows
targetos: Windows
req.lib: 
req.dll: Wmp.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# IWMPEvents3::CdromRipStateChange method


## -description



The <b>CdromRipStateChange</b> event occurs when a CD ripping operation changes state.




## -parameters




### -param pCdromRip [in]

Pointer to the <b>IWMPCdromRip</b> interface that represents the ripping operation that raised the error.


### -param wmprs [in]

<b>WMPRipState</b> enumeration value that indicates the new state.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/c3e2db46-bef0-4c79-91b5-97ca5a86c6ba">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/bd62cae1-3f63-4355-afc7-e429a444189d">WMPRipState</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

