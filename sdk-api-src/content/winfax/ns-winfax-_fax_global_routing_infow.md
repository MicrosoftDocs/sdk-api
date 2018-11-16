---
UID: NS:winfax._FAX_GLOBAL_ROUTING_INFOW
title: "_FAX_GLOBAL_ROUTING_INFOW"
author: windows-sdk-content
description: The FAX_GLOBAL_ROUTING_INFO structure contains information about one fax routing method, as it pertains globally to the fax service.
old-location: fax\_mfax_fax_global_routing_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_07aq.htm
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: "*PFAX_GLOBAL_ROUTING_INFOW, FAX_GLOBAL_ROUTING_INFO, FAX_GLOBAL_ROUTING_INFO structure [Fax Service], FAX_GLOBAL_ROUTING_INFOA, FAX_GLOBAL_ROUTING_INFOW, PFAX_GLOBAL_ROUTING_INFO, PFAX_GLOBAL_ROUTING_INFO structure pointer [Fax Service], _FAX_GLOBAL_ROUTING_INFOW, _mfax_fax_global_routing_info_str, fax._mfax_fax_global_routing_info_str, winfax/FAX_GLOBAL_ROUTING_INFO, winfax/FAX_GLOBAL_ROUTING_INFOA, winfax/FAX_GLOBAL_ROUTING_INFOW, winfax/PFAX_GLOBAL_ROUTING_INFO"
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: struct
req.header: winfax.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: FAX_GLOBAL_ROUTING_INFOW (Unicode) and FAX_GLOBAL_ROUTING_INFOA (ANSI)
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
 - Winfax.h
api_name:
 - FAX_GLOBAL_ROUTING_INFO
 - FAX_GLOBAL_ROUTING_INFOA
 - FAX_GLOBAL_ROUTING_INFOW
product: Windows
targetos: Windows
req.typenames: FAX_GLOBAL_ROUTING_INFOW, *PFAX_GLOBAL_ROUTING_INFOW
req.redist: 
---

# _FAX_GLOBAL_ROUTING_INFOW structure


## -description


The <b>FAX_GLOBAL_ROUTING_INFO</b> structure contains information about one fax routing method, as it pertains globally to the fax service. The structure includes data on the priority level of the fax routing method, and the name of the DLL that exports the routing method. It also includes the GUID and function name that identify the fax routing method, and the method's user-friendly name.

The <b>Guid</b> member is required to identify the fax routing method. Currently the <b>Priority</b> member is the only member that an application can modify.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_GLOBAL_ROUTING_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_GLOBAL_ROUTING_INFO)</b> before it calls the <a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a> function.


### -field Priority

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the priority of the fax routing method. The priority determines the relative order in which the fax service calls the fax routing methods when the service receives a fax document. Valid values for this member are 1 through n, where 1 is the highest priority. 


### -field Guid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For more information about fax routing methods, see <a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">About the Fax Routing Extension API</a>.


### -field FriendlyName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the user-friendly name to display for the fax routing method.


### -field FunctionName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the function that executes the specified fax routing method. The fax routing extension DLL identified by the <b>ExtensionImageName</b> member exports the function.


### -field ExtensionImageName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the fax routing extension DLL that implements the fax routing method.


### -field ExtensionFriendlyName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the user-friendly name to display for the fax routing extension DLL that implements the fax routing method.


## -remarks



A fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a> function to retrieve fax routing method information that applies globally to the fax service. The function returns information about each fax routing method in an individual <b>FAX_GLOBAL_ROUTING_INFO</b> structure.

Call the <a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a> function to modify fax routing method data that applies globally to the fax server, such as routing priority.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms692365(v=VS.85).aspx">Managing Global Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691952(v=VS.85).aspx">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692835(v=VS.85).aspx">FaxEnableRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691941(v=VS.85).aspx">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691451(v=VS.85).aspx">FaxSetGlobalRoutingInfo</a>
 

 

