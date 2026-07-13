---
UID: NS:winfax._FAX_GLOBAL_ROUTING_INFOW
title: FAX_GLOBAL_ROUTING_INFOW (winfax.h)
description: The FAX_GLOBAL_ROUTING_INFO structure contains information about one fax routing method, as it pertains globally to the fax service. (Unicode)
helpviewer_keywords: ["*PFAX_GLOBAL_ROUTING_INFOW","FAX_GLOBAL_ROUTING_INFO","FAX_GLOBAL_ROUTING_INFO structure [Fax Service]","FAX_GLOBAL_ROUTING_INFOA","FAX_GLOBAL_ROUTING_INFOW","PFAX_GLOBAL_ROUTING_INFO","PFAX_GLOBAL_ROUTING_INFO structure pointer [Fax Service]","_mfax_fax_global_routing_info_str","fax._mfax_fax_global_routing_info_str","winfax/FAX_GLOBAL_ROUTING_INFO","winfax/FAX_GLOBAL_ROUTING_INFOA","winfax/FAX_GLOBAL_ROUTING_INFOW","winfax/PFAX_GLOBAL_ROUTING_INFO"]
old-location: fax\_mfax_fax_global_routing_info_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_07aq.htm
ms.date: 12/05/2018
ms.keywords: '*PFAX_GLOBAL_ROUTING_INFOW, FAX_GLOBAL_ROUTING_INFO, FAX_GLOBAL_ROUTING_INFO structure [Fax Service], FAX_GLOBAL_ROUTING_INFOA, FAX_GLOBAL_ROUTING_INFOW, PFAX_GLOBAL_ROUTING_INFO, PFAX_GLOBAL_ROUTING_INFO structure pointer [Fax Service], _mfax_fax_global_routing_info_str, fax._mfax_fax_global_routing_info_str, winfax/FAX_GLOBAL_ROUTING_INFO, winfax/FAX_GLOBAL_ROUTING_INFOA, winfax/FAX_GLOBAL_ROUTING_INFOW, winfax/PFAX_GLOBAL_ROUTING_INFO'
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
targetos: Windows
req.typenames: FAX_GLOBAL_ROUTING_INFOW, *PFAX_GLOBAL_ROUTING_INFOW
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _FAX_GLOBAL_ROUTING_INFOW
 - winfax/_FAX_GLOBAL_ROUTING_INFOW
 - PFAX_GLOBAL_ROUTING_INFOW
 - winfax/PFAX_GLOBAL_ROUTING_INFOW
 - FAX_GLOBAL_ROUTING_INFOW
 - winfax/FAX_GLOBAL_ROUTING_INFOW
dev_langs:
 - c++
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
---

# FAX_GLOBAL_ROUTING_INFOW structure


## -description

The <b>FAX_GLOBAL_ROUTING_INFO</b> structure contains information about one fax routing method, as it pertains globally to the fax service. The structure includes data on the priority level of the fax routing method, and the name of the DLL that exports the routing method. It also includes the GUID and function name that identify the fax routing method, and the method's user-friendly name.

The <b>Guid</b> member is required to identify the fax routing method. Currently the <b>Priority</b> member is the only member that an application can modify.

## -struct-fields

### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_GLOBAL_ROUTING_INFO</b> structure. The calling application must set this member to <b>sizeof(FAX_GLOBAL_ROUTING_INFO)</b> before it calls the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function.

### -field Priority

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the priority of the fax routing method. The priority determines the relative order in which the fax service calls the fax routing methods when the service receives a fax document. Valid values for this member are 1 through n, where 1 is the highest priority.

### -field Guid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 

                    

For more information about fax routing methods, see <a href="/previous-versions/windows/desktop/fax/-mfax-about-the-fax-routing-extension-api">About the Fax Routing Extension API</a>.

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

A fax client application can call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a> function to retrieve fax routing method information that applies globally to the fax service. The function returns information about each fax routing method in an individual <b>FAX_GLOBAL_ROUTING_INFO</b> structure.

Call the <a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a> function to modify fax routing method data that applies globally to the fax server, such as routing priority.

For more information, see <a href="/previous-versions/windows/desktop/fax/-mfax-managing-global-fax-routing-data">Managing Global Fax Routing Data</a>.





> [!NOTE]
> The winfax.h header defines FAX_GLOBAL_ROUTING_INFO as an alias that automatically selects the ANSI or Unicode version of this function based on the definition of the UNICODE preprocessor constant. Mixing usage of the encoding-neutral alias with code that is not encoding-neutral can lead to mismatches that result in compilation or runtime errors. For more information, see [Conventions for Function Prototypes](/windows/win32/intl/conventions-for-function-prototypes).

## -see-also

<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-structures">Fax Service Client API Structures</a>



<a href="/previous-versions/windows/desktop/fax/-mfax-fax-service-client-api-for-windows-2000">Fax Service Client API for Windows 2000</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenableroutingmethoda">FaxEnableRoutingMethod</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumglobalroutinginfoa">FaxEnumGlobalRoutingInfo</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxenumroutingmethodsa">FaxEnumRoutingMethods</a>



<a href="/windows/desktop/api/faxroute/nc-faxroute-pfaxroutemethod">FaxRouteMethod</a>



<a href="/previous-versions/windows/desktop/api/winfax/nf-winfax-faxsetglobalroutinginfoa">FaxSetGlobalRoutingInfo</a>
