---
UID: NS:lmwksta._WKSTA_TRANSPORT_INFO_0
title: WKSTA_TRANSPORT_INFO_0 (lmwksta.h)
description: The WKSTA_TRANSPORT_INFO_0 structure contains information about the workstation transport protocol, such as Wide Area Network (WAN) or NetBIOS.
helpviewer_keywords: ["*LPWKSTA_TRANSPORT_INFO_0","*PWKSTA_TRANSPORT_INFO_0","LPWKSTA_TRANSPORT_INFO_0","LPWKSTA_TRANSPORT_INFO_0 structure pointer [Network Management]","PWKSTA_TRANSPORT_INFO_0","PWKSTA_TRANSPORT_INFO_0 structure pointer [Network Management]","WKSTA_TRANSPORT_INFO_0","WKSTA_TRANSPORT_INFO_0 structure [Network Management]","_win32_wksta_transport_info_0_str","lmwksta/LPWKSTA_TRANSPORT_INFO_0","lmwksta/PWKSTA_TRANSPORT_INFO_0","lmwksta/WKSTA_TRANSPORT_INFO_0","netmgmt.wksta_transport_info_0_str"]
old-location: netmgmt\wksta_transport_info_0_str.htm
tech.root: NetMgmt
ms.assetid: e7afe2a3-f729-4fd5-afc3-d3ffbd09e884
ms.date: 12/05/2018
ms.keywords: '*LPWKSTA_TRANSPORT_INFO_0, *PWKSTA_TRANSPORT_INFO_0, LPWKSTA_TRANSPORT_INFO_0, LPWKSTA_TRANSPORT_INFO_0 structure pointer [Network Management], PWKSTA_TRANSPORT_INFO_0, PWKSTA_TRANSPORT_INFO_0 structure pointer [Network Management], WKSTA_TRANSPORT_INFO_0, WKSTA_TRANSPORT_INFO_0 structure [Network Management], _win32_wksta_transport_info_0_str, lmwksta/LPWKSTA_TRANSPORT_INFO_0, lmwksta/PWKSTA_TRANSPORT_INFO_0, lmwksta/WKSTA_TRANSPORT_INFO_0, netmgmt.wksta_transport_info_0_str'
req.header: lmwksta.h
req.include-header: Lm.h
req.target-type: Windows
req.target-min-winverclnt: Windows 2000 Professional [desktop apps only]
req.target-min-winversvr: Windows 2000 Server [desktop apps only]
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
targetos: Windows
req.typenames: WKSTA_TRANSPORT_INFO_0, *PWKSTA_TRANSPORT_INFO_0, *LPWKSTA_TRANSPORT_INFO_0
req.redist: 
ms.custom: 19H1
f1_keywords:
 - _WKSTA_TRANSPORT_INFO_0
 - lmwksta/_WKSTA_TRANSPORT_INFO_0
 - PWKSTA_TRANSPORT_INFO_0
 - lmwksta/PWKSTA_TRANSPORT_INFO_0
 - WKSTA_TRANSPORT_INFO_0
 - lmwksta/WKSTA_TRANSPORT_INFO_0
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - HeaderDef
api_location:
 - Lmwksta.h
api_name:
 - WKSTA_TRANSPORT_INFO_0
---

# WKSTA_TRANSPORT_INFO_0 structure


## -description

The 
				<b>WKSTA_TRANSPORT_INFO_0</b> structure contains information about the workstation transport protocol, such as Wide Area Network (WAN) or NetBIOS.

## -struct-fields

### -field wkti0_quality_of_service

Specifies a value that determines the search order of the transport protocol with respect to other transport protocols. The highest value is searched first.

### -field wkti0_number_of_vcs

Specifies the number of clients communicating with the server using this transport protocol.

### -field wkti0_transport_name

Specifies the device name of the transport protocol.

### -field wkti0_transport_address

Specifies the address of the server on this transport protocol.

This string is Unicode if  <b>_WIN32_WINNT</b> or <b>FORCE_UNICODE</b> are defined.

### -field wkti0_wan_ish

This member is ignored by the 
<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd">NetWkstaTransportAdd</a> function. For the 
<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportenum">NetWkstaTransportEnum</a> function, this member indicates whether the transport protocol is a WAN transport protocol. This member is set to <b>TRUE</b> for NetBIOS/TCIP; it is set to <b>FALSE</b> for NetBEUI and NetBIOS/IPX. 




Certain legacy networking protocols, including NetBEUI, will no longer be supported. For more information, see 
<a href="/windows/desktop/WinSock/network-protocol-support-in-windows">Network Protocol Support in Windows</a>.

## -see-also

<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportadd">NetWkstaTransportAdd</a>



<a href="/windows/desktop/api/lmwksta/nf-lmwksta-netwkstatransportenum">NetWkstaTransportEnum</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management Overview</a>



<a href="/windows/desktop/NetMgmt/network-management-structures">Network Management Structures</a>



<a href="/windows/desktop/NetMgmt/server-and-workstation-transport-functions">Server and Workstation Transport Functions</a>