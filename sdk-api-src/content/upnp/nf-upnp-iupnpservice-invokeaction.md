---
UID: NF:upnp.IUPnPService.InvokeAction
title: IUPnPService::InvokeAction
author: windows-sdk-content
description: Invokes a method on the device.
old-location: upnp\iupnpservice_invokeaction.htm
tech.root: UPnP
ms.assetid: fe8b4761-63cb-46a9-a7d0-5603cc1a5a58
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: IUPnPService interface [UPnP APIs],InvokeAction method, IUPnPService.InvokeAction, IUPnPService::InvokeAction, InvokeAction, InvokeAction method [UPnP APIs], InvokeAction method [UPnP APIs],IUPnPService interface, _upnp_iupnpservice_invokeaction, upnp.iupnpservice_invokeaction, upnp/IUPnPService::InvokeAction
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: upnp.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
req.target-min-winversvr: None supported
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
req.dll: Upnp.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Upnp.dll
api_name:
 - IUPnPService.InvokeAction
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- COM
: 
- upnp.h
: 
- IUPnPService.InvokeAction
: 
---

# IUPnPService::InvokeAction


## -description


The 
<b>InvokeAction</b> method invokes a method on the device.


## -parameters




### -param bstrActionName [in]

Specifies the method to invoke.


### -param vInActionArgs

TBD


### -param pvOutActionArgs

TBD


### -param pvRetVal

TBD




#### - pvarOutActionArgs [in, out]

On input, contains a reference to an empty array. On output, receives a reference to the array of output arguments. If the action has no output arguments, this parameter contains an empty array. 
						

The contents of this parameter are service-specific.

Free this parameter with <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.
						


#### - pvarRetVal [in, out]

On input, contains a reference to an empty array. On output, receives a reference to a <b>VARIANT</b> that contains the return value of this action.

If the device returns an error after the action is invoked on it and this parameter is not set to <b>NULL</b>, this parameter will contain specific text describing the error upon return. For more information on the errors returned by devices, please refer to the <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a> documentation.

Free this parameter with <a href="28741d81-8404-4f85-95d3-5c209ec13835">VariantClear</a>.
						


#### - varInActionArgs [in]

Specifies an array of input arguments to the method. If the action has no input arguments, this parameter must contain an empty array. 




The contents of this array are service-specific.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in WinError.h or one of the UPnP-specific return values shown in the following table. Some of these values indicate that an error was received from a UPnP-certified device. For more information, see <a href="https://msdn.microsoft.com/4b18a5d4-f6e8-4670-93dd-ecd012940000">Device Error Codes</a>.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ACTION_REQUEST_FAILED</b></dt>
</dl>
</td>
<td width="60%">
The device had an internal error; the request could not be executed.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An unknown error occurred.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_DEVICE_TIMEOUT</b></dt>
</dl>
</td>
<td width="60%">
The device has not responded within the 30 second time-out period.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_ERROR_PROCESSING_RESPONSE</b></dt>
</dl>
</td>
<td width="60%">
The device has sent a response that cannot be processed; for example, the response was corrupted.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ACTION</b></dt>
</dl>
</td>
<td width="60%">
The action is not supported by the device.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_INVALID_ARGUMENTS</b></dt>
</dl>
</td>
<td width="60%">
One or more of the arguments passed in <i>vInActionArgs</i> is invalid.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_PROTOCOL_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred at the UPnP control-protocol level.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>UPNP_E_TRANSPORT_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An HTTP error occurred. Use the <a href="https://msdn.microsoft.com/8593b800-ae0a-41b8-9a61-92bdfc106c8b">IUPnPService::LastTransportStatus</a> property to obtain the actual HTTP status code.

<div class="alert"><b>Note</b>  This error code is also returned when the SOAP response exceeds 100 kilobytes.</div>
<div> </div>
</td>
</tr>
</table>
 




## -remarks



When an application invokes the method <b>InvokeAction</b>, it includes a list of arguments that should match the arguments expected by the service. The Control Point maps these <b>VARIANT</b> arguments to the required type. The following table shows the mappings that are used.

<table>
<tr>
<th>Data type</th>
<th>Type returned by MSXML</th>
</tr>
<tr>
<td>
<b>SDT_STRING</b> = 0

</td>
<td><b>VT_BSTR</b></td>
</tr>
<tr>
<td><b>SDT_NUMBER</b></td>
<td><b>VT_BSTR</b></td>
</tr>
<tr>
<td><b>SDT_INT</b></td>
<td><b>VT_I4</b></td>
</tr>
<tr>
<td><b>SDT_FIXED_14_4</b></td>
<td><b>VT_CY</b></td>
</tr>
<tr>
<td><b>SDT_BOOLEAN</b></td>
<td><b>VT_BOOL</b></td>
</tr>
<tr>
<td><b>SDT_DATETIME_ISO8601</b></td>
<td><b>VT_DATE</b></td>
</tr>
<tr>
<td><b>SDT_DATETIME_ISO8601TZ</b></td>
<td><b>VT_DATE</b></td>
</tr>
<tr>
<td><b>SDT_DATE_ISO8601</b></td>
<td><b>VT_DATE</b></td>
</tr>
<tr>
<td><b>SDT_TIME_ISO8601</b></td>
<td><b>VT_DATE</b></td>
</tr>
<tr>
<td><b>SDT_TIME_ISO8601TZ</b></td>
<td><b>VT_DATE</b></td>
</tr>
<tr>
<td><b>SDT_I1</b></td>
<td><b>VT_I1</b></td>
</tr>
<tr>
<td><b>SDT_I2</b></td>
<td><b>VT_I2</b></td>
</tr>
<tr>
<td><b>SDT_I4</b></td>
<td><b>VT_I4</b></td>
</tr>
<tr>
<td><b>SDT_UI1</b></td>
<td><b>VT_UI1</b></td>
</tr>
<tr>
<td><b>SDT_UI2</b></td>
<td><b>VT_UI2</b></td>
</tr>
<tr>
<td><b>SDT_UI4</b></td>
<td><b>VT_UI4</b></td>
</tr>
<tr>
<td><b>SDT_R4</b></td>
<td><b>VT_FLOAT</b></td>
</tr>
<tr>
<td><b>SDT_R8</b></td>
<td><b>VT_DOUBLE</b></td>
</tr>
<tr>
<td><b>SDT_FLOAT</b></td>
<td><b>VT_DOUBLE</b></td>
</tr>
<tr>
<td><b>SDT_UUID</b></td>
<td><b>VT_BSTR</b></td>
</tr>
<tr>
<td><b>SDT_BIN_BASE64</b></td>
<td><b>VT_ARRAY</b></td>
</tr>
<tr>
<td><b>SDT_BIN_HEX</b></td>
<td><b>VT_ARRAY</b></td>
</tr>
<tr>
<td><b>SDT_CHAR</b></td>
<td>
<b>VT_UI2</b> (a wchar)

</td>
</tr>
<tr>
<td><b>SDT_URI</b></td>
<td><b>VT_BSTR</b></td>
</tr>
</table>
 

<div class="alert"><b>Note</b>  Parameters that receive values must not be passed a <b>NULL</b> value when the method is called.</div>
<div> </div>
<div class="alert"><b>Note</b>  A floating-point value sent by a device as an [out] argument or a return value will be changed when received by the control point. For example, consider a device with an action Action1Out_float that returns a single [out] floating-point argument. When a control point invokes this action, the device returns the value -234.567; however, the control point actually receives the value -234.567001342773 instead of the expected value -234.567.<p class="note">To work around this issue, use r4 instead of float as the UPnP data type for non-integer numeric values.

</div>
<div> </div>



## -see-also




<a href="https://msdn.microsoft.com/48b20b03-62a4-4dcd-8eda-f1bfef1eef38">IUPnPService</a>
 

 

