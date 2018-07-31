---
UID: NF:winfax.FaxEnumRoutingMethodsW
title: FaxEnumRoutingMethodsW function
author: windows-sdk-content
description: The FaxEnumRoutingMethods function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application.
old-location: fax\_mfax_faxenumroutingmethods.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_41gz.htm
ms.author: windowssdkdev
ms.date: 07/29/2018
ms.keywords: FaxEnumRoutingMethods, FaxEnumRoutingMethods function [Fax Service], FaxEnumRoutingMethodsA, FaxEnumRoutingMethodsW, _mfax_faxenumroutingmethods, fax._mfax_faxenumroutingmethods, winfax/FaxEnumRoutingMethods, winfax/FaxEnumRoutingMethodsA, winfax/FaxEnumRoutingMethodsW
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
req.unicode-ansi: FaxEnumRoutingMethodsW (Unicode) and FaxEnumRoutingMethodsA (ANSI)
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
 - FaxEnumRoutingMethods
 - FaxEnumRoutingMethodsA
 - FaxEnumRoutingMethodsW
product: Windows
targetos: Windows
req.lib: WinFax.lib
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# FaxEnumRoutingMethodsW function


## -description


The <b>FaxEnumRoutingMethods</b> function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a> function.


### -param RoutingMethod [out]

Type: <b>PFAX_ROUTING_METHOD*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/592c5437-3712-4f45-9817-dcfe5c3480b0">FAX_ROUTING_METHOD</a> structures. Each structure contains information about one fax routing method. The data includes, among other items, the name of the DLL that exports the routing method, the GUID and function name that identify the routing method, and the method's user-friendly name. 

                    

For information about memory allocation, see the following Remarks section. For information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>.


### -param MethodsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/592c5437-3712-4f45-9817-dcfe5c3480b0">FAX_ROUTING_METHOD</a> structures the <b>FaxEnumRoutingMethods</b> function returns in the <i>RoutingMethod</i> parameter.


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
One or all of the <i>MethodsReturned</i>, <i>RoutingMethod</i>, or <i>FaxPortHandle</i> parameters are <b>NULL</b>.

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
</table>
 




## -remarks



A fax administration application typically calls the <b>FaxEnumRoutingMethods</b> function to query the fax routing methods associated with a particular device. A call to the <a href="https://msdn.microsoft.com/4b75f71e-c432-4003-b307-6e85fe0e21dd">FaxSetRoutingInfo</a> function changes the routing information for a particular fax routing method.

The <a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxEnumRoutingMethods</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/592c5437-3712-4f45-9817-dcfe5c3480b0">FAX_ROUTING_METHOD</a> buffer array pointed to by the <i>RoutingMethod</i> parameter. An application must call the <a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/49416909-d475-4c76-ae2a-bd3c39611b32">Fax Server Configuration Management</a> and <a href="https://msdn.microsoft.com/a8371d98-8a66-484a-9179-4894ae0a7dfc">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/df832bcb-d07f-454b-b571-43854706a6c1">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/592c5437-3712-4f45-9817-dcfe5c3480b0">FAX_ROUTING_METHOD</a>



<a href="https://msdn.microsoft.com/b076b5ba-09af-4312-90c1-27abd0b859df">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/99d8053a-f994-456e-814c-9584705aa278">FaxEnableRoutingMethod</a>



<a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/9a7eedc8-e00f-40e8-a9f4-8e919012ed47">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/c13d203d-e7b1-4bc6-a875-04ddd981d549">FaxGetRoutingInfo</a>



<a href="https://msdn.microsoft.com/9010d651-3259-40b2-91bf-de0a841207c1">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a>



<b>FaxSetRoutingInfo</b>
 

 

