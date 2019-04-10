---
UID: NS:winsvc._SERVICE_TRIGGER_SPECIFIC_DATA_ITEM
title: SERVICE_TRIGGER_SPECIFIC_DATA_ITEM (winsvc.h)
author: windows-sdk-content
description: Contains trigger-specific data for a service trigger event.
old-location: base\service_trigger_specific_data_item.htm
tech.root: Services
ms.assetid: 670e6c49-bbc0-4af6-9e47-6c89801ebb45
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PSERVICE_TRIGGER_SPECIFIC_DATA_ITEM, PSERVICE_TRIGGER_SPECIFIC_DATA_ITEM, PSERVICE_TRIGGER_SPECIFIC_DATA_ITEM structure pointer, SERVICE_TRIGGER_DATA_TYPE_BINARY, SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ALL, SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ANY, SERVICE_TRIGGER_DATA_TYPE_LEVEL, SERVICE_TRIGGER_DATA_TYPE_STRING, SERVICE_TRIGGER_SPECIFIC_DATA_ITEM, SERVICE_TRIGGER_SPECIFIC_DATA_ITEM structure, base.service_trigger_specific_data_item, winsvc/PSERVICE_TRIGGER_SPECIFIC_DATA_ITEM, winsvc/SERVICE_TRIGGER_SPECIFIC_DATA_ITEM"
ms.topic: struct
req.header: winsvc.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - winsvc.h
api_name:
 - SERVICE_TRIGGER_SPECIFIC_DATA_ITEM
product: Windows
targetos: Windows
req.typenames: SERVICE_TRIGGER_SPECIFIC_DATA_ITEM, *PSERVICE_TRIGGER_SPECIFIC_DATA_ITEM
req.redist: 
---

# SERVICE_TRIGGER_SPECIFIC_DATA_ITEM structure


## -description


Contains trigger-specific data for a service trigger event. This structure is used by the <a href="https://msdn.microsoft.com/a57aa702-40a2-4880-80db-6c4f43c3e7ea">SERVICE_TRIGGER</a> structure for SERVICE_TRIGGER_TYPE_CUSTOM, SERVICE_TRIGGER_TYPE_DEVICE_ARRIVAL, SERVICE_TRIGGER_TYPE_FIREWALL_PORT_EVENT, or SERVICE_TRIGGER_TYPE_NETWORK_ENDPOINT trigger events. 


## -struct-fields




### -field dwDataType

The data type of the trigger-specific data pointed to by <b>pData</b>. This member can be one of the following values. 

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TRIGGER_DATA_TYPE_BINARY"></a><a id="service_trigger_data_type_binary"></a><dl>
<dt><b>SERVICE_TRIGGER_DATA_TYPE_BINARY</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
The trigger-specific data is in binary format.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TRIGGER_DATA_TYPE_STRING"></a><a id="service_trigger_data_type_string"></a><dl>
<dt><b>SERVICE_TRIGGER_DATA_TYPE_STRING</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
The trigger-specific data is in string format. 

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TRIGGER_DATA_TYPE_LEVEL"></a><a id="service_trigger_data_type_level"></a><dl>
<dt><b>SERVICE_TRIGGER_DATA_TYPE_LEVEL</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
The trigger-specific data is a byte value. 

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ANY"></a><a id="service_trigger_data_type_keyword_any"></a><dl>
<dt><b>SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ANY</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
The trigger-specific data is a 64-bit unsigned integer value.

</td>
</tr>
<tr>
<td width="40%"><a id="SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ALL"></a><a id="service_trigger_data_type_keyword_all"></a><dl>
<dt><b>SERVICE_TRIGGER_DATA_TYPE_KEYWORD_ALL</b></dt>
<dt>5</dt>
</dl>
</td>
<td width="60%">
The trigger-specific data is a 64-bit unsigned integer value.

</td>
</tr>
</table>
 


### -field cbData

The size of the trigger-specific data pointed to <b>pData</b>, in bytes.  The maximum value is 1024.


### -field cbData.range

 


### -field cbData.range.0

 


### -field cbData.range.1024

 


### -field pData

A pointer to the trigger-specific data for the service trigger event. The trigger-specific data depends on the trigger event type; see Remarks. 

If the <b>dwDataType</b> member is SERVICE_TRIGGER_DATA_TYPE_BINARY, the trigger-specific data is an array of bytes. 

If the <b>dwDataType</b> member is SERVICE_TRIGGER_DATA_TYPE_STRING, the trigger-specific data is a null-terminated string or a multistring of null-terminated strings, ending with two null-terminating characters. For example: <code>"5001\0UDP\0%programfiles%\MyApplication\MyServiceProcess.exe\0MyService\0\0"</code>.

Strings must be Unicode; ANSI strings are not supported.


### -field pData.size_is

 


### -field pData.size_is.cbData

 




## -remarks



The following table lists trigger-specific data by trigger event type. 

<table>
<tr>
<th>Event type</th>
<th>Trigger-specific data</th>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_CUSTOM</td>
<td>Specified by the <a href="http://go.microsoft.com/fwlink/p/?linkid=133390">Event Tracing for Windows</a> (ETW) provider that defines the custom event.</td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_DEVICE_INTERFACE_ARRIVAL</td>
<td>A SERVICE_TRIGGER_DATA_TYPE_STRING string that specifies a hardware ID or compatible ID string for the device interface class.  </td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_DOMAIN_JOIN</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_FIREWALL_PORT_EVENT</td>
<td>A SERVICE_TRIGGER_DATA_TYPE_STRING multi-string that specifies the port, the protocol, and optionally the executable path and name of the service listening on the event. </td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_GROUP_POLICY</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_IP_ADDRESS_AVAILABILITY</td>
<td>Not applicable.</td>
</tr>
<tr>
<td>SERVICE_TRIGGER_TYPE_NETWORK_ENDPOINT</td>
<td>A SERVICE_TRIGGER_DATA_TYPE_STRING that specifies the port, named pipe, or RPC interface for the network endpoint.</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/6e5b79ed-52e1-460e-b076-01afbd08775c">ChangeServiceConfig2</a>



<a href="https://msdn.microsoft.com/cb090e59-aeff-4420-bb7c-912a4911006f">QueryServiceConfig2</a>



<a href="https://msdn.microsoft.com/a57aa702-40a2-4880-80db-6c4f43c3e7ea">SERVICE_TRIGGER</a>



<a href="https://msdn.microsoft.com/ca02a3ae-b16a-4427-b6db-b935c9cf23b3">Service Trigger Events</a>
 

 

