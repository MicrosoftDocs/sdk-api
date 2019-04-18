---
UID: NS:faxroute._FAX_ROUTE
title: FAX_ROUTE (faxroute.h)
author: windows-sdk-content
description: The FAX_ROUTE structure contains information about a received fax document. The fax service passes the structure to a fax routing method in a call to the FaxRouteMethod function.
old-location: fax\_mfax_fax_route_str.htm
tech.root: Fax
ms.assetid: VS|fax|~\fax\faxrouteextapiref_3gj6.htm
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: "*PFAX_ROUTE, FAX_ROUTE, FAX_ROUTE structure [Fax Service], PFAX_ROUTE, PFAX_ROUTE structure pointer [Fax Service], _mfax_fax_route_str, fax._mfax_fax_route_str, faxroute/FAX_ROUTE, faxroute/PFAX_ROUTE"
ms.topic: struct
req.header: faxroute.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional, Windows XP [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
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
 - FaxRoute.h
api_name:
 - FAX_ROUTE
product: Windows
targetos: Windows
req.typenames: FAX_ROUTE, *PFAX_ROUTE
req.redist: 
ms.custom: 19H1
---

# FAX_ROUTE structure


## -description


The <b>FAX_ROUTE</b> structure contains information about a received fax document. The fax service passes the structure to a fax routing method in a call to the <a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a> function.


## -struct-fields




### -field SizeOfStruct

Type: <b>DWORD</b>

Specifies, in bytes, the size of the <b>FAX_ROUTE</b> structure. Before calling the <a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a> function, the fax service sets this member to sizeof(FAX_ROUTE).


### -field JobId

Type: <b>DWORD</b>

Specifies a unique number that identifies the fax job that received the fax document.


### -field ElapsedTime

Type: <b>DWORDLONG</b>

Specifies a 64-bit unsigned integer that is the elapsed time, in UTC, for the fax job that received the fax document. This parameter represents the total time that elapses between the beginning of fax reception and the end of fax reception.


### -field ReceiveTime

Type: <b>DWORDLONG</b>

Specifies a 64-bit unsigned integer that is the starting time, in UTC, for the fax job that received the fax document.


### -field PageCount

Type: <b>DWORD</b>

Specifies the number of pages in the received fax document.


### -field Csid

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the called station identifier of the local fax device that received the fax document. This identifier is usually a telephone number.


### -field Tsid

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the transmitting station identifier of the remote fax device that sent the fax document. This identifier is usually a telephone number.


### -field CallerId

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that identifies the calling device that sent the fax document. This string may include the telephone number of the calling device.


### -field RoutingInfo

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the routing string for the received fax document. The string must be of the form: 

                    

<code>Canonical-Phone-Number[|Additional-Routing-Info]</code>

where <code>Canonical-Phone-Number</code> is defined in the <a href="https://msdn.microsoft.com/en-us/library/ms726017(v=VS.85).aspx">Address</a> topic of the TAPI documentation (see the Canonical Address subheading); and <code>Additional-Routing-Info</code> is the <i>subaddress</i> of a Canonical Address, and uses the subaddress format.


### -field ReceiverName

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the name of the person who received the fax document.


### -field ReceiverNumber

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the telephone number of the fax device that received the fax document.


### -field DeviceName

Type: <b>LPCWSTR</b>

Pointer to a constant null-terminated Unicode character string that specifies the name of the device that received the fax document.


### -field DeviceId

Type: <b>DWORD</b>

Specifies the permanent line identifier for the receiving fax device. 


### -field RoutingInfoData

Type: <b>LPBYTE</b>

Pointer to a buffer that contains additional routing data defined by the routing extension. For more information, see the following Remarks section.


### -field RoutingInfoDataSize

Type: <b>DWORD</b>

Specifies the size, in bytes, of the array pointed to by the <b>RoutingInfoData</b> member.


## -remarks



A fax routing method can call the <a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a> callback function to change the routing information for a subsequent routing method. The function does this by modifying the <b>RoutingInfoData</b> member of the <b>FAX_ROUTE</b> structure that applies to the subsequent method. This allows a fax routing extension to retrieve user-defined routing data and to provide additional callback information to a different routing method. When the subsequent routing method executes, it processes the received fax transmission using the modified routing data. For more information, see <b>FaxRouteModifyRoutingData</b>.

The fax routing method can use the <a href="https://msdn.microsoft.com/58dfce16-2d7f-4db5-9f84-5dd651d26745">FileTimeToLocalFileTime</a> function, to convert from UTC to local time, and then use the <a href="https://msdn.microsoft.com/d1d55f1f-4daa-4b9d-9962-873e38b1e0cf">FileTimeToSystemTime</a> function to convert the local time to a <a href="https://msdn.microsoft.com/f77cdf86-0f97-4a89-b565-95b46fa7d65b">SYSTEMTIME</a> structure. SYSTEMTIME contains individual members for month, day, year, weekday, hour, minute, second, and millisecond. See MSDN for descriptions of these functions and this structure.




## -see-also




<a href="https://msdn.microsoft.com/en-us/library/ms684519(v=VS.85).aspx">Fax Routing Extension Application Programming Interface Overview</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692900(v=VS.85).aspx">Fax Routing Extension Structures</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692857(v=VS.85).aspx">FaxRouteMethod</a>



<a href="https://msdn.microsoft.com/en-us/library/ms692909(v=VS.85).aspx">FaxRouteModifyRoutingData</a>
 

 

