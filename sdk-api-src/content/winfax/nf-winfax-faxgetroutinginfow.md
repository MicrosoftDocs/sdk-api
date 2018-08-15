---
UID: NF:winfax.FaxGetRoutingInfoW
title: FaxGetRoutingInfoW function
author: windows-sdk-content
description: The FaxGetRoutingInfo function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device.
old-location: fax\_mfax_faxgetroutinginfo.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_1pwv.htm
ms.author: windowssdkdev
ms.date: 08/03/2018
ms.keywords: FaxGetRoutingInfo, FaxGetRoutingInfo function [Fax Service], FaxGetRoutingInfoA, FaxGetRoutingInfoW, _mfax_faxgetroutinginfo, fax._mfax_faxgetroutinginfo, winfax/FaxGetRoutingInfo, winfax/FaxGetRoutingInfoA, winfax/FaxGetRoutingInfoW
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: winfax.h
req.include-header: 
req.redist: 
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

# FaxGetRoutingInfoW function


## -description


The <b>FaxGetRoutingInfo</b> function returns to a fax client application routing information for a fax routing method that is associated with a specific fax device.


## -parameters




### -param FaxPortHandle [in]

Type: <b>HANDLE</b>

Specifies a fax port handle returned by a call to the <a href="https://msdn.microsoft.com/en-us/library/ms690875(v=VS.85).aspx">FaxOpenPort</a> function.


### -param RoutingGuid [in]

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest.
                    
                    

For information about fax routing methods, see <a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">About the Fax Routing Extension API</a>. For information about the relationship between routing methods and GUIDs, see <a href="https://msdn.microsoft.com/en-us/library/ms691955(v=VS.85).aspx">Fax Routing Methods</a>.


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

An application that manages a specific fax routing method can call the <b>FaxGetRoutingInfo</b> function to modify the routing information for the method on a specified fax device. To enumerate all fax routing methods associated with a device, call the <a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a> function.

The <a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a> function retrieves routing information that applies globally to the fax server, such as routing priority. An application can modify global data with a call to the <a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a> function.

The <b>FaxGetRoutingInfo</b> function allocates the memory required for the buffer pointed to by the <i>RoutingInfoBuffer</i> parameter. An application must call the <a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a> function to deallocate the resources associated with this parameter.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691940(v=VS.85).aspx">Managing Fax Routing Data</a> and <a href="https://msdn.microsoft.com/en-us/library/ms690878(v=VS.85).aspx">Freeing Fax Resources</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms690746(v=VS.85).aspx">FAX_GLOBAL_ROUTING_INFO</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691947(v=VS.85).aspx">Fax Service Client API Functions</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692846(v=VS.85).aspx">FaxFreeBuffer</a>



<a href="https://msdn.microsoft.com/en-us/library/ms690875(v=VS.85).aspx">FaxOpenPort</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691949(v=VS.85).aspx">FaxSetRoutingInfo</a>
 

 

