---
UID: NF:strmif.IAMResourceControl.Reserve
title: IAMResourceControl::Reserve
author: windows-sdk-content
description: The Reserve method reserves or unreserves a device resource.
old-location: dshow\iamresourcecontrol_reserve.htm
old-project: DirectShow
ms.assetid: 5f264b87-dae4-4478-811f-1c99e670928a
ms.author: windowssdkdev
ms.date: 08/02/2018
ms.keywords: IAMResourceControl interface [DirectShow],Reserve method, IAMResourceControl.Reserve, IAMResourceControl::Reserve, IAMResourceControlReserve, Reserve, Reserve method [DirectShow], Reserve method [DirectShow],IAMResourceControl interface, dshow.iamresourcecontrol_reserve, strmif/IAMResourceControl::Reserve
ms.prod: windows
ms.technology: windows-sdk
ms.topic: method
req.header: strmif.h
req.include-header: Dshow.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
tech.root: 
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Strmiids.lib
 - Strmiids.dll
api_name:
 - IAMResourceControl.Reserve
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMResourceControl::Reserve


## -description



The <code>Reserve</code> method reserves or unreserves a device resource.




## -parameters




### -param dwFlags [in]

Flag indicating whether to reserve or unreserve this device. The value must be a member of the <a href="https://msdn.microsoft.com/528c4e2e-2045-45a1-b502-75e103745c93">AMRESCTL_RESERVEFLAGS</a> enumeration.


### -param pvReserved [in]

Must be <b>NULL</b>.


## -returns



Returns S_OK if the device was successfully reserved or unreserved, S_FALSE if the device is currently reserved and will continue to be held, or an <b>HRESULT</b> error code if the device can't be reserved.




## -remarks



A resource can be reserved multiple times. If the method returns S_OK, the filter increments an internal reserve count. For every call to reserve a device that returns S_OK, the caller must make a matching call to unreserve the device.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/9b0b6b46-bf61-44c2-981a-44df4d7c6dfb">IAMResourceControl Interface</a>
 

 

