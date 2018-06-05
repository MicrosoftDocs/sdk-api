---
UID: NS:winfax._FAX_GLOBAL_ROUTING_INFOW
title: "_FAX_GLOBAL_ROUTING_INFOW"
author: windows-sdk-content
description: The FAX_GLOBAL_ROUTING_INFO structure contains information about one fax routing method, as it pertains globally to the fax service.
old-location: fax\_mfax_fax_global_routing_info_str.htm
old-project: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_07aq.htm
ms.author: windowssdkdev
ms.date: 05/21/2018
ms.keywords: "*PFAX_GLOBAL_ROUTING_INFOW, FAX_GLOBAL_ROUTING_INFO, FAX_GLOBAL_ROUTING_INFO structure [Fax Service], FAX_GLOBAL_ROUTING_INFOA, FAX_GLOBAL_ROUTING_INFOW, PFAX_GLOBAL_ROUTING_INFO, PFAX_GLOBAL_ROUTING_INFO structure pointer [Fax Service], _FAX_GLOBAL_ROUTING_INFOW, _mfax_fax_global_routing_info_str, fax._mfax_fax_global_routing_info_str, winfax/FAX_GLOBAL_ROUTING_INFO, winfax/FAX_GLOBAL_ROUTING_INFOA, winfax/FAX_GLOBAL_ROUTING_INFOW, winfax/PFAX_GLOBAL_ROUTING_INFO"
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: FAX_GLOBAL_ROUTING_INFOW, *PFAX_GLOBAL_ROUTING_INFOW
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	HeaderDef
api_location:
-	Winfax.h
api_name:
-	FAX_GLOBAL_ROUTING_INFO
-	FAX_GLOBAL_ROUTING_INFOA
-	FAX_GLOBAL_ROUTING_INFOW
product: Windows
targetos: Windows
req.lib: 
req.dll: 
req.irql: 
req.product: Windows Address Book 5.0
---

# _FAX_GLOBAL_ROUTING_INFOW structure


## -description


The <b>FAX_GLOBAL_ROUTING_INFO</b> structure contains information about one fax routing method, as it pertains globally to the fax service. The structure includes data on the priority level of the fax routing method, and the name of the DLL that exports the routing method. It also includes the GUID and function name that identify the fax routing method, and the method's user-friendly name.

The <b>Guid</b> member is required to identify the fax routing method. Currently the <b>Priority</b> member is the only member that an application can modify.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_GLOBAL_ROUTING_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_GLOBAL_ROUTING_INFO)</b> before it calls the <a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a> function.


### -field Priority

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the priority of the fax routing method. The priority determines the relative order in which the fax service calls the fax routing methods when the service receives a fax document. Valid values for this member are 1 through n, where 1 is the highest priority. 


### -field Guid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For more information about fax routing methods, see <a href="https://msdn.microsoft.com/f8bdf0de-9455-45d1-9271-3929e0429d5c">About the Fax Routing Extension API</a>.


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



A fax client application can call the <a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a> function to retrieve fax routing method information that applies globally to the fax service. The function returns information about each fax routing method in an individual <b>FAX_GLOBAL_ROUTING_INFO</b> structure.

Call the <a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a> function to modify fax routing method data that applies globally to the fax server, such as routing priority.

For more information, see <a href="https://msdn.microsoft.com/858b2326-7634-4021-8cff-128bbc167aba">Managing Global Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/be81e221-4aba-4c63-9640-337bee49fdb4">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/cbc79dc5-d0ca-418d-8572-64b0a582056f">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/99d8053a-f994-456e-814c-9584705aa278">FaxEnableRoutingMethod</a>



<a href="https://msdn.microsoft.com/776b1a16-9a5f-458b-96ee-b2f41568b7e5">FaxEnumGlobalRoutingInfo</a>



<a href="https://msdn.microsoft.com/1f78fed5-6b49-4946-8607-f1d7f9052aaa">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/c9220335-bb45-48b3-b303-b6ea10260952">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/bd831edb-8fb9-4338-93fb-da07ac3a5a56">FaxSetGlobalRoutingInfo</a>
 

 

