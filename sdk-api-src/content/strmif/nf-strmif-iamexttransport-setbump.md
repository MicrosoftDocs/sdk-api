---
UID: NF:strmif.IAMExtTransport.SetBump
title: IAMExtTransport::SetBump
author: windows-sdk-content
description: The SetBump method temporarily changes the playback, for synchronization of multiple external devices.
old-location: dshow\iamexttransport_setbump.htm
old-project: DirectShow
ms.assetid: c2f2b59f-2522-4f13-8861-fb4e2d9d406c
ms.author: windowssdkdev
ms.date: 05/29/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetBump method, IAMExtTransport.SetBump, IAMExtTransport::SetBump, IAMExtTransportSetBump, SetBump, SetBump method [DirectShow], SetBump method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_setbump, strmif/IAMExtTransport::SetBump
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
req.typenames: DVD_RELATIVE_BUTTON
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	Strmiids.lib
-	Strmiids.dll
api_name:
-	IAMExtTransport.SetBump
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::SetBump


## -description



The <code>SetBump</code> method temporarily changes the playback, for synchronization of multiple external devices.



This method is not implemented.


## -parameters




### -param Speed [in]

Specifies the temporary speed (a multiple of normal speed) as a <b>long</b> integer.


### -param Duration [in]

Specifies the duration of a bump as a <b>long</b> integer. The duration is given in the current time format; see <a href="https://msdn.microsoft.com/798fa8d0-3834-4168-86a6-069cae3c3e8e">IAMExtTransport::SetTransportBasicParameters</a> for more information.


## -returns



Returns an <b>HRESULT</b> value that depends on the implementation of the interface.




## -remarks



This method causes a temporary speed variation of the transport. The transport operates at the new speed until the specified duration elapses. Then it returns to its previous speed.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/340b7c9a-cfd9-4915-b0fc-0d12d7663578">IAMExtTransport::GetBump</a>
 

 

