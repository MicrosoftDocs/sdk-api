---
UID: NF:dhcpsapi.DhcpAddServer
title: DhcpAddServer function
author: windows-sdk-content
description: The DhcpAddServer function attempts to add a new server to the existing list of DHCP servers maintained in the domain directory service. If the specified DHCP server already exists in the directory service, an error is returned.
old-location: dhcp\dhcpaddserver.htm
tech.root: DHCP
ms.assetid: bdf5d239-478a-47af-9240-19d1b6933f7e
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: DhcpAddServer, DhcpAddServer function [DHCP], dhcp.dhcpaddserver, dhcpsapi/DhcpAddServer
ms.prod: windows-hardware
ms.technology: windows-devices
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
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpsapi.dll
api_name:
 - DhcpAddServer
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# DhcpAddServer function


## -description


The <b>DhcpAddServer</b> function attempts to add a new server to the existing list of DHCP servers maintained in the domain directory service. If the specified DHCP server  already exists in the directory service, an error is returned.


## -parameters




### -param Flags [in]

Reserved for future use. This field should be set to 0x00000000.


### -param IdInfo [in]

Pointer to an address containing the server's ID block. This field should be set to null.


### -param NewServer [in]

Pointer to a <a href="https://msdn.microsoft.com/12f3fbd3-9b81-4a11-914c-83658c2bce89">DHCP_SERVER_INFO</a> structure containing information about the new DHCP server. The <b>DsLocation</b> and <b>DsLocType</b> members present in this structure are not valid in this implementation, and they should be set to null. The <b>Version</b> member of this structure should be set to 0.


### -param CallbackFn [in]

Pointer to the callback function that will be called when the server add operation completes. This field should be null.


### -param CallbackData [in]

Pointer to a data block containing the formatted structure for callback information. This field should be null.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.




## -see-also




<a href="https://msdn.microsoft.com/12f3fbd3-9b81-4a11-914c-83658c2bce89">DHCP_SERVER_INFO</a>



<a href="https://msdn.microsoft.com/88b6c29b-7b01-40c7-b4f5-4920845f1eb9">DhcpDeleteServer</a>
 

 

