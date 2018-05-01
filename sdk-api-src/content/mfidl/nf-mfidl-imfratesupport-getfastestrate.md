---
UID: NF:mfidl.IMFRateSupport.GetFastestRate
title: IMFRateSupport::GetFastestRate method
author: windows-driver-content
description: Gets the fastest playback rate supported by the object.
old-location: mf\imfratesupport_getfastestrate.htm
old-project: medfound
ms.assetid: 00413771-21cb-48a7-9080-2c3d195c366b
ms.author: windowsdriverdev
ms.date: 4/23/2018
ms.keywords: 00413771-21cb-48a7-9080-2c3d195c366b, GetFastestRate method [Media Foundation], GetFastestRate method [Media Foundation], IMFRateSupport interface, GetFastestRate,IMFRateSupport.GetFastestRate, IMFRateSupport, IMFRateSupport interface [Media Foundation], GetFastestRate method, IMFRateSupport::GetFastestRate, mf.imfratesupport_getfastestrate, mfidl/IMFRateSupport::GetFastestRate
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: mfidl.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps | UWP apps]
req.target-min-winversvr: Windows Server 2008 [desktop apps | UWP apps]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.typenames: MF_URL_TRUST_STATUS
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	COM
api_location:
-	mfuuid.lib
-	mfuuid.dll
api_name:
-	IMFRateSupport.GetFastestRate
product: Windows
targetos: Windows
req.lib: Mfuuid.lib
req.dll: 
req.irql: 
req.product: GDI+ 1.1
---

# IMFRateSupport::GetFastestRate method


## -description



Gets the fastest playback rate supported by the object.




## -parameters




### -param eDirection [in]

Specifies whether to query to the fastest forward playback rate or reverse playback rate. The value is a member of the <a href="https://msdn.microsoft.com/34cc861c-ab15-48f4-bb6e-736b70383546">MFRATE_DIRECTION</a> enumeration.


### -param fThin [in]

If <b>TRUE</b>, the method retrieves the fastest thinned playback rate. Otherwise, the method retrieves the fastest non-thinned playback rate. For information about thinning, see <a href="https://msdn.microsoft.com/509b2cc8-6017-41a9-ae80-9af21dce9367">About Rate Control</a>.


### -param pflRate [out]

Receives the fastest playback rate that the object supports.


## -returns



The method returns an <b>HRESULT</b>. Possible values include, but are not limited to, those in the following table.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
The method succeeded.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_REVERSE_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support reverse playback.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>MF_E_THINNING_UNSUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
The object does not support thinning.

</td>
</tr>
</table>
 




## -remarks



For some formats (such as ASF), thinning means dropping all frames that are not I-frames. If a component produces stream data, such as a media source or a demultiplexer, it should pay attention to the <i>fThin</i> parameter and return MF_E_THINNING_UNSUPPORTED if it cannot thin the stream.

If the component processes or receives a stream (most transforms or media sinks), it may ignore this parameter if it does not care whether the stream is thinned. In the Media Session's implementation of rate support, if the transforms do not explicitly support reverse playback, the Media Session will attempt to playback in reverse with thinning but not without thinning. Therefore, most applications will set <i>fThin</i> to <b>TRUE</b> when using the Media Session for reverse playback.

If <i>eDirection</i> is MFRATE_REVERSE, the method retrieves the fastest reverse playback rate. This is a negative value, assuming the object supports reverse playback.




## -see-also




<a href="https://msdn.microsoft.com/7f2b64e1-1062-4f77-b8e0-62b6d962ae8b">How to Determine Supported Rates</a>



<a href="https://msdn.microsoft.com/a6c495fa-0f6a-4e4c-8fba-996b22d55053">IMFRateSupport</a>
 

 

