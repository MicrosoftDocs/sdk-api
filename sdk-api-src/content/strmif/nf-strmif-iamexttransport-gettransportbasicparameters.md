---
UID: NF:strmif.IAMExtTransport.GetTransportBasicParameters
title: IAMExtTransport::GetTransportBasicParameters
author: windows-sdk-content
description: The GetTransportBasicParameters method retrieves general properties of the external transport.
old-location: dshow\iamexttransport_gettransportbasicparameters.htm
old-project: DirectShow
ms.assetid: 7f670efe-4433-496d-b789-925c02b69f58
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: GetTransportBasicParameters, GetTransportBasicParameters method [DirectShow], GetTransportBasicParameters method [DirectShow],IAMExtTransport interface, IAMExtTransport interface [DirectShow],GetTransportBasicParameters method, IAMExtTransport.GetTransportBasicParameters, IAMExtTransport::GetTransportBasicParameters, IAMExtTransportGetTransportBasicParameters, dshow.iamexttransport_gettransportbasicparameters, strmif/IAMExtTransport::GetTransportBasicParameters
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
 - IAMExtTransport.GetTransportBasicParameters
product: Windows
targetos: Windows
req.lib: Strmiids.lib
req.dll: 
req.irql: 
req.product: Windows XP with SP1
---

# IAMExtTransport::GetTransportBasicParameters


## -description



The <code>GetTransportBasicParameters</code> method retrieves general properties of the external transport.




## -parameters




### -param Param [in]

Specifies which property to receive.


### -param pValue [in, out]

Pointer to a variable that receives a <b>long</b> integer value. See Remarks for more information.


### -param ppszData [in, out]

Pointer to a variable of type <b>LPOLESTR</b> that receives a string. See Remarks for more information.


## -returns



When this method succeeds, it returns S_OK. Otherwise it returns an <b>HRESULT</b> error code.




## -remarks



The <i>Param</i> parameter is a flag that specifies which property to retrieve. Some properties are numeric; these are returned in the <i>pValue</i> parameter. Other properties are string values; these are returned in the <i>ppszData</i> parameter. For a list of flags and expected values, see <a href="https://msdn.microsoft.com/798fa8d0-3834-4168-86a6-069cae3c3e8e">IAMExtTransport::SetTransportBasicParameters</a>.

If the method returns a string, the caller must free the string, using the <a href="https://msdn.microsoft.com/3d0af12e-fc74-4ef7-b2dd-e9da5d0483c7">CoTaskMemFree</a> function.

<h3><a id="DV_and_MPEG_Camcorder_Implementation"></a><a id="dv_and_mpeg_camcorder_implementation"></a><a id="DV_AND_MPEG_CAMCORDER_IMPLEMENTATION"></a>DV and MPEG Camcorder Implementation</h3>

<a href="https://msdn.microsoft.com/146ca753-fe41-49d3-8b1c-077e10a28192">MSDV</a> supports the following additional flags:

<ul>
<li>
ED_RAW_EXT_DEV_CMD: Invokes a raw AV/C command. Specify the AV/C command as an array of bytes in the <i>ppszData</i> parameter. Specify the size of the command, in bytes, in the <i>pValue</i> parameter. When the method returns, <i>ppszData</i> contains the response from the device, and <i>pValue</i> contains the size of the response, in bytes. The AV/C command is passed directly to the device with no validation or error checking.

The response payload might be larger than the command. It is the caller's responsibility to allocate enough space in the buffer for the response. The maximum payload size is 512 bytes.

For more information, see <a href="https://msdn.microsoft.com/18081652-962f-4605-84b7-1fa60f61ad05">Issuing Raw AV/C Commands</a>.

</li>
<li>
ED_TRANSBASIC_INPUT_SIGNAL: Retrieves the signal format that the DV camcorder is designed to accept. Returns one of the following constants in <i>pValue</i>.

<table>
<tr>
<th>Constant</th>
<th>Description </th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_SD</td>
<td>NTSC SD signal. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_SDL</td>
<td>NTSC SDL (long-play) signal. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_SD</td>
<td>PAL SD signal.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_SDL</td>
<td>PAL SDL (long-play) signal.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_MPEG2TS</td>
<td>D-VHS signal.</td>
</tr>
</table>
 

</li>
<li>ED_TRANSBASIC_OUTPUT_SIGNAL: Retrieves the signal format that the DV camcorder is designed to transmit. Returns one of the constants listed for the ED_TRANSBASIC_INPUT_SIGNAL flag. 
</li>
</ul>

<a href="https://msdn.microsoft.com/aa59f322-09b1-4b0a-be6f-d865c20f76e5">MSTape</a> supports additional values for ED_TRANSBASIC_INPUT_SIGNAL and ED_TRANSBASIC_OUTPUT_SIGNAL.

<table>
<tr>
<th>Constant</th>
<th>Description </th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_2500_60_MPEG</td>
<td>25-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_1250_60_MPEG</td>
<td>12.5-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_0625_60_MPEG</td>
<td>6.25-Mbps/60 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_2500_50_MPEG</td>
<td>25-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_1250_50_MPEG</td>
<td>12.5-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_0625_50_MPEG</td>
<td>6.25-Mbps/50 MPEG stream.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_UNKNOWN</td>
<td>Unknown signal format.</td>
</tr>
</table>
 

These flags are defined in the header file Xprtdefs.h.

In Windows XP Service Pack 2 and later, the following additional signal types are defined for the ED_TRANSBASIC_INPUT_SIGNAL and ED_TRANSBASIC_OUTPUT_SIGNAL flags.

<table>
<tr>
<th>Constant</th>
<th>Description</th>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_DV25</td>
<td>DVCPRO 25, 525-60.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_DV25</td>
<td>DVCPRO 25, 625-50. </td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_525_60_DV50</td>
<td>DVCPRO 50, 525-60.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_625_50_DV50</td>
<td>DVCPRO 50, 625-50.</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_HD_60_DVH1</td>
<td>DVCPRO 100, 1080i or 720p</td>
</tr>
<tr>
<td>ED_TRANSBASIC_SIGNAL_HD_50_DVH1</td>
<td>DVCPRO 100, 1080i only</td>
</tr>
</table>
 

To use these constants, include the header file Xprtdefs.h from the Windows SDK.




## -see-also




<a href="https://msdn.microsoft.com/369c2bd1-9c11-4524-b999-6a3b73c45261">Error and Success Codes</a>



<a href="https://msdn.microsoft.com/4ce48038-bfcf-4b1f-8053-3446929a5f06">IAMExtTransport Interface</a>
 

 

