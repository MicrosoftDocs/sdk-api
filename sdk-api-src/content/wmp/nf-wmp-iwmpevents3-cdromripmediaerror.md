---
UID: NF:wmp.IWMPEvents3.CdromRipMediaError
title: IWMPEvents3::CdromRipMediaError (wmp.h)
author: windows-sdk-content
description: The CdromRipMediaError event occurs when an error happens while ripping an individual track from a CD.
old-location: wmp\iwmpevents3_iwmpevents3__cdromripmediaerror.htm
tech.root: WMP
ms.assetid: 103f6d52-5b59-422d-918d-5004cbdfc75a
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: CdromRipMediaError, CdromRipMediaError method [Windows Media Player], CdromRipMediaError method [Windows Media Player],IWMPEvents3 interface, IWMPEvents3 interface [Windows Media Player],CdromRipMediaError method, IWMPEvents3.CdromRipMediaError, IWMPEvents3::CdromRipMediaError, IWMPEvents3CdromRipMediaError, wmp.iwmpevents3_iwmpevents3__cdromripmediaerror, wmp/IWMPEvents3::CdromRipMediaError
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
 - IWMPEvents3.CdromRipMediaError
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IWMPEvents3::CdromRipMediaError


## -description



The <b>CdromRipMediaError</b> event occurs when an error happens while ripping an individual track from a CD.




## -parameters




### -param pCdromRip [in]

Pointer to the <b>IWMPCdromRip</b> interface that represents the ripping operation that raised the error.


### -param pMedia [in]

Pointer to the <b>IDispatch</b> interface that represents the media item that raised the error. Call <b>QueryInterface</b> through this pointer to retrieve a pointer to <b>IWMPMedia</b>.


## -returns



This method does not return a value.




## -remarks



You can also handle this event through an <b>IDispatch</b> event sink by using the <b>_WMPOCXEvents</b> interface.

<b>Windows Media Player 10 Mobile: </b>This event is not supported.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/Dd563102(v=VS.85).aspx">IWMPCdromRip Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563296(v=VS.85).aspx">IWMPEvents3 Interface</a>



<a href="https://msdn.microsoft.com/en-us/library/Dd563397(v=VS.85).aspx">IWMPMedia Interface</a>



<a href="https://msdn.microsoft.com/883d538e-19b6-417b-a32d-622c41c24b9c">_WMPOCXEvents Interface</a>
 

 

