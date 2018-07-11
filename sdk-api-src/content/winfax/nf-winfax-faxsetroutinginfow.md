---
UID: NF:winfax.FaxSetRoutingInfoW
title: FaxSetRoutingInfoW function
author: windows-sdk-content
description: A fax management application calls the FaxSetRoutingInfo function to modify the routing information for a fax routing method that is associated with a specific fax device.
old-location: fax\_mfax_faxsetroutinginfo.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_66i7.htm
ms.author: windowssdkdev
ms.date: 06/12/2018
ms.keywords: FaxSetRoutingInfo, FaxSetRoutingInfo function [Fax Service], FaxSetRoutingInfoA, FaxSetRoutingInfoW, _mfax_faxsetroutinginfo, fax._mfax_faxsetroutinginfo, winfax/FaxSetRoutingInfo, winfax/FaxSetRoutingInfoA, winfax/FaxSetRoutingInfoW
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: EVT_VARIANT, *PEVT_VARIANT
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
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxSetRoutingInfoW function


## -description


A fax management application calls the <b>FaxSetRoutingInfo</b> function to modify the routing information for a fax routing method that is associated with a specific fax device.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/library/ms690875(v=VS.85).aspx">FaxOpenPort</a> function.


### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For information about fax routing methods, see <a href="https://msdn.microsoft.com/library/ms684519(v=VS.85).aspx">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="https://msdn.microsoft.com/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.


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
Access is denied. <a href="https://msdn.microsoft.com/library/ms692302(v=VS.85).aspx">FAX_PORT_SET</a> access is required.

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

To obtain a valid port handle to specify in the <i>FaxPortHandle</i> parameter of the <b>FaxSetRoutingInfo</b> function, call the <a href="https://msdn.microsoft.com/library/ms690875(v=VS.85).aspx">FaxOpenPort</a> function.

The <a href="https://msdn.microsoft.com/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a> function.

For more information, see <a href="https://msdn.microsoft.com/library/ms691940(v=VS.85).aspx">Managing Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/library/ms690746(v=VS.85).aspx">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/library/ms690904(v=VS.85).aspx">FaxGetRoutingInfo</a>



<a href="https://msdn.microsoft.com/library/ms690875(v=VS.85).aspx">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a>
 

 

