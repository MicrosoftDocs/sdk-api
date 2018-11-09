---
UID: NF:winfax.FaxEnumRoutingMethodsA
title: FaxEnumRoutingMethodsA function
author: windows-sdk-content
description: The FaxEnumRoutingMethods function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application.
old-location: fax\_mfax_faxenumroutingmethods.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_41gz.htm
ms.author: windowssdkdev
ms.date: 11/05/2018
ms.keywords: FaxEnumRoutingMethods, FaxEnumRoutingMethods function [Fax Service], FaxEnumRoutingMethodsA, FaxEnumRoutingMethodsW, _mfax_faxenumroutingmethods, fax._mfax_faxenumroutingmethods, winfax/FaxEnumRoutingMethods, winfax/FaxEnumRoutingMethodsA, winfax/FaxEnumRoutingMethodsW
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
req.unicode-ansi: FaxEnumRoutingMethodsW (Unicode) and FaxEnumRoutingMethodsA (ANSI)
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
 - FaxEnumRoutingMethods
 - FaxEnumRoutingMethodsA
 - FaxEnumRoutingMethodsW
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# FaxEnumRoutingMethodsA function


## -description


The <b>FaxEnumRoutingMethods</b> function enumerates all fax routing methods for a specific fax device. The function returns information about each routing method to a fax client application.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms690875(v=VS.85).aspx">FaxOpenPort</a> function.


### -param RoutingMethod [out]

Type: <b>PFAX_ROUTING_METHOD*</b>

Pointer to the address of a buffer to receive an array of <a href="https://msdn.microsoft.com/en-us/library/ms692354(v=VS.85).aspx">FAX_ROUTING_METHOD</a> structures. Each structure contains information about one fax routing method. The data includes, among other items, the name of the DLL that exports the routing method, the GUID and function name that identify the routing method, and the method's user-friendly name. 

                    

For information about memory allocation, see the following Remarks section. For information about fax routing methods, see <a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">About the Fax Routing Extension API</a>.


### -param MethodsReturned [out]

Type: <b>LPDWORD</b>

Pointer to a <b>DWORD</b> variable to receive the number of <a href="https://msdn.microsoft.com/en-us/library/ms692354(v=VS.85).aspx">FAX_ROUTING_METHOD</a> structures the <b>FaxEnumRoutingMethods</b> function returns in the <i>RoutingMethod</i> parameter.


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
Access is denied. <a href="https://msdn.microsoft.com/en-us/library/ms692302(v=VS.85).aspx">FAX_PORT_QUERY</a> access is required.

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



A fax administration application typically calls the <b>FaxEnumRoutingMethods</b> function to query the fax routing methods associated with a particular device. A call to the <a href="https://msdn.microsoft.com/en-us/library/ms691949(v=VS.85).aspx">FaxSetRoutingInfo</a> function changes the routing information for a particular fax routing method.

The <a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxEnumRoutingMethods</b> function allocates the memory required for the <a href="https://msdn.microsoft.com/en-us/library/ms692354(v=VS.85).aspx">FAX_ROUTING_METHOD</a> buffer array pointed to by the <i>RoutingMethod</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691849(v=VS.85).aspx">Fax Server Configuration Management</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690746(v=VS.85).aspx">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692354(v=VS.85).aspx">FAX_ROUTING_METHOD</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692835(v=VS.85).aspx">FaxEnableRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690904(v=VS.85).aspx">FaxGetRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690875(v=VS.85).aspx">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a>



<b>FaxSetRoutingInfo</b>
 

 

