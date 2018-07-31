---
UID: NF:winfax.FaxGetRoutingInfoA
title: FaxGetRoutingInfoA function
author: windows-sdk-content
description: The FaxGetRoutingInfo function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device.
old-location: fax\_mfax_faxgetroutinginfo.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1pwv.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FaxGetRoutingInfo, FaxGetRoutingInfo function [Fax Service], FaxGetRoutingInfoA, FaxGetRoutingInfoW, _mfax_faxgetroutinginfo, fax._mfax_faxgetroutinginfo, winfax/FaxGetRoutingInfo, winfax/FaxGetRoutingInfoA, winfax/FaxGetRoutingInfoW
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
req.unicode-ansi: FaxGetRoutingInfoW (Unicode) and FaxGetRoutingInfoA (ANSI)
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
 - FaxGetRoutingInfo
 - FaxGetRoutingInfoA
 - FaxGetRoutingInfoW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxGetRoutingInfoA function


## -description


The <b>FaxGetRoutingInfo</b> function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest.
                    
                    

For information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="https://msdn.microsoft.com/a2144af9-9101-478f-93b9-393101dc1936">Fax Routing Methods</a>.


### -param RoutingInfoBuffer [out]

Type: <b>LPBYTE*</b>

Pointer to the address of a buffer to receive the fax routing information.


### -param RoutingInfoBufferSize [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the size of the buffer, in bytes, pointed to by the <i>RoutingInfoBuffer</i> parameter.


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
Access is denied. <a href="https://msdn.microsoft.com/7d6ff208-33e4-42b2-ae21-76ec8ff58809">FAX_PORT_QUERY</a> access is required.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
One or all of the <i>RoutingGuid</i>, <i>RoutingInfoBuffer</i>, <i>RoutingInfoBufferSize</i>, or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_ENOUGH_MEMORY</b></dt>
</dl>
</td>
<td width="60%">
An error occurred during memory allocation.

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



The fax service administration application, a Microsoft Management Console (MMC) snap-in component that manages the specified fax routing method, typically calls the <b>FaxGetRoutingInfo</b> function. This is because the format of the routing data is unavailable to a fax client application. The routing data is relevant only to the exported fax routing method and to the fax service administration application.

An application that manages a specific fax routing method can call the <b>FaxGetRoutingInfo</b> function to modify the routing information for the method on a specified fax device. To enumerate all fax routing methods associated with a device, call the <a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a> function.

The <a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxGetRoutingInfo</b> function allocates the memory required for the buffer pointed to by the <i>RoutingInfoBuffer</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/356dda5c-852e-46b7-8fa4-f3a0c62d65cb">Managing Fax Routing Data</a> and <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/df832bcb-d07f-454b-b571-43854706a6c1">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/4b75f71e-c432-4003-b307-6e85fe0e21dd">FaxSetRoutingInfo</a>
 

 

