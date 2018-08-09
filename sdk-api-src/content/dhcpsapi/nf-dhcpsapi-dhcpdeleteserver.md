---
UID: NF:dhcpsapi.DhcpDeleteServer
title: DhcpDeleteServer function
author: windows-sdk-content
description: The DhcpDeleteServer function attempts to delete a DHCP server and any related objects (such as subnet information and IP reservations) from the directory service.
old-location: dhcp\dhcpdeleteserver.htm
old-project: dhcp
ms.assetid: 88b6c29b-7b01-40c7-b4f5-4920845f1eb9
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: DhcpDeleteServer, DhcpDeleteServer function [DHCP], dhcp.dhcpdeleteserver, dhcpsapi/DhcpDeleteServer
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: QuarantineStatus
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpDeleteServer
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpDeleteServer function


## -description


The <b>DhcpDeleteServer</b> function attempts to delete a DHCP server and any related objects (such as subnet information and IP reservations) from the directory service.


## -parameters




### -param Flags [in]

Set to zero.


### -param IdInfo [in]

Set to null.


### -param NewServer [in]

Pointer to a <a href="https://msdn.microsoft.com/12f3fbd3-9b81-4a11-914c-83658c2bce89">DHCP_SERVER_INFO</a> structure that contains the details of the DHCP server to delete from the directory service.


### -param CallbackFn [in]

Pointer to the function to call after this operation is executed. Set to null.


### -param CallbackData [in]

Pointer to the list of data that will be passed to the callback function specified in <i>CallbackFn</i>. Set to null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/12f3fbd3-9b81-4a11-914c-83658c2bce89">DHCP_SERVER_INFO</a>



<a href="https://msdn.microsoft.com/c8b4d241-19d4-4a97-9129-c2954d63b6ac">DhcpEnumServers</a>
 

 

