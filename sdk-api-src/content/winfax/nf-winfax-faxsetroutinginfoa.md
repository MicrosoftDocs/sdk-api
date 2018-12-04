---
UID: NF:winfax.FaxSetRoutingInfoA
title: FaxSetRoutingInfoA function
author: windows-sdk-content
description: A fax management application calls the FaxSetRoutingInfo function to modify the routing information for a fax routing method that is associated with a specific fax device.
old-location: fax\_mfax_faxsetroutinginfo.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_66i7.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: FaxSetRoutingInfo, FaxSetRoutingInfo function [Fax Service], FaxSetRoutingInfoA, FaxSetRoutingInfoW, _mfax_faxsetroutinginfo, fax._mfax_faxsetroutinginfo, winfax/FaxSetRoutingInfo, winfax/FaxSetRoutingInfoA, winfax/FaxSetRoutingInfoW
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FaxSetRoutingInfoW (Unicode) and FaxSetRoutingInfoA (ANSI)
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: WinFax.lib
req.dll: 
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - LibDef
api_location:
 - WinFax.lib
 - WinFax.dll
api_name:
 - FaxSetRoutingInfo
 - FaxSetRoutingInfoA
 - FaxSetRoutingInfoW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxSetRoutingInfoA function


## -description


A fax management application calls the <b>FaxSetRoutingInfo</b> function to modify the routing information for a fax routing method that is associated with a specific fax device.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.


### -param RoutingInfoBuffer [in]

Type: <b>const BYTE*</b>

Pointer to a buffer that contains the fax routing information. The routing data is typically provided by the fax service administration application, a MMC snap-in component.


### -param RoutingInfoBufferSize [in]

Type: <b>DWORD</b>

Pointer to a <b>DWORD</b> variable that contains the size of the buffer, in bytes, pointed to by the <i>RoutingInfoBuffer</i> parameter.


## -returns



Type: <b>BOOL</b>

If the function succeeds, the return value is nonzero.

If the function fails, the return value is zero. To get extended error information, call <a href="https://msdn.microsoft.com/d852e148-985c-416f-a5a7-27b6914b45d4">GetLastError</a>. GetLastError can return one of the following errors.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_ACCESS_DENIED</b></dt>
</dl>
</td>
<td width="60%">
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_SET</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or more of the parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_DATA</b></dt>
</dl>
</td>
<td width="60%">
The <i>RoutingGuid</i> parameter is invalid.

</td>
</tr>
</table>
 




## -remarks



The fax service administration application, an MMC snap-in component that manages the specified fax routing method, typically calls the <b>FaxSetRoutingInfo</b> function. This is because the format of the routing data is unavailable to the fax client application. The routing data is relevant only to the exported fax routing method and the method's administration application.

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter of the <b>FaxSetRoutingInfo</b> function, call the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.

The <a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a> function.

For more information, see <a href="https://msdn.microsoft.com/356dda5c-852e-46b7-8fa4-f3a0c62d65cb">Managing Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/df832bcb-d07f-454b-b571-43854706a6c1">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/c13d203d-e7b1-4bc6-a875-04ddd981d549">FaxGetRoutingInfo</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a>
 

 

