---
UID: NF:wmp.IWMPEvents3.CdromBurnStateChange
title: IWMPEvents3::CdromBurnStateChange
author: windows-sdk-content
description: The CdromBurnStateChange event occurs when a CD burning operation changes state.
old-location: wmp\iwmpevents3_iwmpevents3__cdromburnstatechange.htm
tech.root: WMP
ms.assetid: 8328f1bf-c928-4504-859f-f1b62e77e9e0
ms.author: windowssdkdev
ms.date: 09/27/2018
ms.keywords: CdromBurnStateChange, CdromBurnStateChange method [Windows Media Player], CdromBurnStateChange method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromBurnStateChange method, IWMPEvents3.CdromBurnStateChange, IWMPEvents3::CdromBurnStateChange, IWMPEvents3CdromBurnStateChange, wmp.iwmpevents3_iwmpevents3__cdromburnstatechange, wmp/IWMPEvents3::CdromBurnStateChange
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
 - IWMPEvents3.CdromBurnStateChange
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
- IWMPEvents3.CdromBurnStateChange
: 
---

# IWMPEvents3::CdromBurnStateChange


## -description



The <b>CdromBurnStateChange</b> event occurs when a CD burning operation changes state.




## -parameters




### -param pCdromBurn [in]

Pointer to the <b>IWMPCdromBurn</b> interface that represents the burning operation that raised the event.


### -param wmpbs [in]

<b>WMPBurnState</b> enumeration value that indicates the new state.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/45116a33-62f9-4c7d-b246-25905cbaf118">IWMPCdromBurn Interface</a>



<a href="https://msdn.microsoft.com/654b7d78-97d4-4770-9729-dd1fed0431d9">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/fd286f68-4d36-48ae-800e-ad2be4c613c1">WMPBurnState</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

