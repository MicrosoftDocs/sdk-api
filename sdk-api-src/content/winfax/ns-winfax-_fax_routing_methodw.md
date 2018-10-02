---
UID: NS:winfax._FAX_ROUTING_METHODW
title: "_FAX_ROUTING_METHODW"
author: windows-sdk-content
description: The FAX_ROUTING_METHOD structure contains information about one fax routing method, as it pertains to one fax device.
old-location: fax\_mfax_fax_routing_method_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxlegacy_7w1e.htm
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: "*PFAX_ROUTING_METHODW, FAX_ROUTING_METHOD, FAX_ROUTING_METHOD structure [Fax Service], FAX_ROUTING_METHODA, FAX_ROUTING_METHODW, PFAX_ROUTING_METHOD, PFAX_ROUTING_METHOD structure pointer [Fax Service], _FAX_ROUTING_METHODW, _mfax_fax_routing_method_str, fax._mfax_fax_routing_method_str, winfax/FAX_ROUTING_METHOD, winfax/FAX_ROUTING_METHODA, winfax/FAX_ROUTING_METHODW, winfax/PFAX_ROUTING_METHOD"
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
req.unicode-ansi: FAX_ROUTING_METHODW (Unicode) and FAX_ROUTING_METHODA (ANSI)
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
 - FAX_ROUTING_METHOD
 - FAX_ROUTING_METHODA
 - FAX_ROUTING_METHODW
product: Windows
targetos: Windows
req.typenames: FAX_ROUTING_METHODW, *PFAX_ROUTING_METHODW
req.redist: 
---

# _FAX_ROUTING_METHODW structure


## -description


The <b>FAX_ROUTING_METHOD</b> structure contains information about one fax routing method, as it pertains to one fax device. The data includes, among other items, whether the fax routing method is enabled for the device, and the name of the DLL that exports the routing method. It also includes the GUID and function name that uniquely identify the routing method, and the method's user-friendly name.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies the size, in bytes, of the <b>FAX_ROUTING_METHOD</b> structure. The fax service sets this member to <b>sizeof(FAX_ROUTING_METHOD)</b>. 


### -field DeviceId

Type: <b>DWORD</b>

Specifies a <b>DWORD</b> variable that indicates the permanent line identifier for the fax device of interest. 


### -field Enabled

Type: <b>BOOL</b>

Specifies a Boolean variable that indicates whether the fax routing method is enabled or disabled for the fax device of interest. If this parameter is equal to <b>TRUE</b>, the fax routing method is enabled for the device. 


### -field DeviceName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the fax device of interest. 


### -field Guid

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the GUID that uniquely identifies the fax routing method of interest. 
                
                    

For more information about fax routing methods, see <a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">About the Fax Routing Extension API</a>. 


### -field FriendlyName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the user-friendly name to display for the fax routing method. 


### -field FunctionName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that is the name of the function that executes the specified fax routing procedure. The fax routing extension DLL identified by the <b>ExtensionImageName</b> member exports the function. 


### -field ExtensionImageName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the name of the fax routing extension DLL that implements the fax routing method.


### -field ExtensionFriendlyName

Type: <b>LPCTSTR</b>

Pointer to a constant null-terminated character string that specifies the user-friendly name to display for the fax routing extension DLL. 


## -remarks



A fax client application can call the <a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a> function to enumerate all the fax routing methods associated with a specific fax device. The function returns an array of <b>FAX_ROUTING_METHOD</b> structures. Each structure describes one fax routing method in detail.

Call the <a href="https://msdn.microsoft.com/en-us/library/ms692835(v=VS.85).aspx">FaxEnableRoutingMethod</a> function to enable or disable a fax routing method for a specific fax device.

For more information, see <a href="https://msdn.microsoft.com/en-us/library/ms691940(v=VS.85).aspx">Managing Fax Routing Data</a>.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms691952(v=VS.85).aspx">Fax Service Client API Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692829(v=VS.85).aspx">Fax Service Client API for Windows 2000</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692835(v=VS.85).aspx">FaxEnableRoutingMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms691804(v=VS.85).aspx">FaxEnumRoutingMethods</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>
 

 

