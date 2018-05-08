---
UID: NF:strmif.IAMExtTransport.SetChase
title: IAMExtTransport::SetChase
author: windows-driver-content
description: The SetChase method enables or disables chase mode.
old-location: dshow\iamexttransport_setchase.htm
old-project: DirectShow
ms.assetid: f8c94e74-e243-4fa9-85e6-8c027b514e4f
ms.author: windowsdriverdev
ms.date: 4/30/2018
ms.keywords: IAMExtTransport interface [DirectShow],SetChase method, IAMExtTransport.SetChase, IAMExtTransport::SetChase, IAMExtTransportSetChase, SetChase, SetChase method [DirectShow], SetChase method [DirectShow],IAMExtTransport interface, dshow.iamexttransport_setchase, strmif/IAMExtTransport::SetChase
ms.prod: windows-hardware
ms.technology: windows-devices
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
-	IAMExtTransport.SetChase
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::SetChase


## -description



The <code>SetChase</code> method enables or disables chase mode.



This method is not implemented.


## -parameters




### -param Enable [in]

Specifies whether chase is enabled as a <b>long</b> integer.

<table>
<tr>
<th>
                  Value
                </th>
<th>
                  Description
                </th>
</tr>
<tr>
<td>OATRUE</td>
<td>Enable chase.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Disable chase.</td>
</tr>
</table>
 


### -param Offset [in]

Specifies the offset that the transport will maintain from a reference time. The offset is given in the current time format; see <a href="https://msdn.microsoft.com/798fa8d0-3834-4168-86a6-069cae3c3e8e">IAMExtTransport::SetTransportBasicParameters</a> for more information.


### -param hEvent [in]

Specifies a handle to an event. The device signals the event after it has established the signal offset.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Use this method when you want an external transport to follow a timecode signal by a fixed offset. For example, if a VCR supports chasing, it can switch to play mode and keep the tape at a fixed offset from a reference timecode.

Chase mode remains in effect until it completes or is canceled. The filter must verify that the transport is maintaining the fixed offset, by periodically reading the transport's timecode.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/9ef12fa0-2ec9-45e5-9c22-20f810dac73b">IAMExtTransport::GetChase</a>
 

 

