---
UID: NF:strmif.IAMExtTransport.put_EditStart
title: IAMExtTransport::put_EditStart method
author: windows-driver-content
description: The put_EditStart method activates the edit control on a capable transport.
old-location: dshow\iamexttransport_put_editstart.htm
old-project: DirectShow
ms.assetid: 1fd9c788-2ccb-47e5-bed8-fece9cfdf2a6
ms.author: windowsdriverdev
ms.date: 4/26/2018
ms.keywords: IAMExtTransport, IAMExtTransport interface [DirectShow], put_EditStart method, IAMExtTransport::put_EditStart, IAMExtTransportput_EditStart, dshow.iamexttransport_put_editstart, put_EditStart method [DirectShow], put_EditStart method [DirectShow], IAMExtTransport interface, put_EditStart,IAMExtTransport.put_EditStart, strmif/IAMExtTransport::put_EditStart
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
-	IAMExtTransport.put_EditStart
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::put_EditStart method


## -description



The <code>put_EditStart</code> method activates the edit control on a capable transport.



This method is not implemented.


## -parameters




### -param Value [in]

Specifies whether to active the edit control.

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
<td>Activates the edit control.</td>
</tr>
<tr>
<td>OAFALSE</td>
<td>Deactivates the edit control.</td>
</tr>
</table>
 


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



Use this method to manually enable edit control. Edit control is defined as the precise enabling of individual, or a set of, record tracks on a VCR; for example, a video-only insert edit, where only the video record head is enabled and a new video signal is recorded—the audio signal is left as is. Use this method to control "on the fly" editing on machines that have this feature.

<h3><a id="DV_Implementation"></a><a id="dv_implementation"></a><a id="DV_IMPLEMENTATION"></a>DV Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> does not support this method. It returns E_NOTIMPL.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>



<a href="https://msdn.microsoft.com/83eb6f22-646c-400a-8adb-5545914656c9">IAMExtTransport::get_EditStart</a>
 

 

