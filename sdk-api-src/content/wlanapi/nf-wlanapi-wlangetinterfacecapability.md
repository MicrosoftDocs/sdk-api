---
UID: NF:wlanapi.WlanGetInterfaceCapability
title: WlanGetInterfaceCapability function
author: windows-sdk-content
description: Retrieves the capabilities of an interface.
old-location: nwifi\wlangetinterfacecapability.htm
old-project: nativewifi
ms.assetid: 09f8273a-5259-44fa-b55e-af3282735c0b
ms.author: windowssdkdev
ms.date: 08/06/2018
ms.keywords: WlanGetInterfaceCapability, WlanGetInterfaceCapability function [NativeWIFI], nwifi.wlangetinterfacecapability, wlanapi/WlanGetInterfaceCapability
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: wlanapi.h
req.include-header: Wlanapi.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2008 [desktop apps only]
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
req.typenames: WL_DISPLAY_PAGES, *PWL_DISPLAY_PAGES
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - wlanapi.dll
api_name:
 - WlanGetInterfaceCapability
product: Windows
targetos: Windows
req.lib: Wlanapi.lib
req.dll: Wlanapi.dll
req.irql: 
req.product: Windows XP Professional x64 Edition or 64-bit editions of     Windows Server 2003
---

# WlanGetInterfaceCapability function


## -description


The <b>WlanGetInterfaceCapability</b> function retrieves the capabilities of an interface.


## -parameters




### -param hClientHandle [in]

The client's session handle, obtained by a previous call to the <a href="https://msdn.microsoft.com/27bfa0c1-4443-47a4-a374-326f553fa3bb">WlanOpenHandle</a> function.


### -param pInterfaceGuid [in]

The GUID of this interface.


### -param pReserved

Reserved for future use.  Must be set to <b>NULL</b>.


### -param ppCapability [out]

A <a href="https://msdn.microsoft.com/db7a9066-d699-4860-90cd-dc3f4bf42549">WLAN_INTERFACE_CAPABILITY</a> structure that contains information about the capabilities of the specified interface.


## -returns



If the function succeeds, the return value is ERROR_SUCCESS.

If the function fails, the return value may be one of the following return codes.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_PARAMETER</b></dt>
</dl>
</td>
<td width="60%">
<i>hClientHandle</i> is <b>NULL</b> or invalid,  <i>pInterfaceGuid</i> is <b>NULL</b>, <i>pReserved</i> is not <b>NULL</b>, or <i>ppCapability</i> is <b>NULL</b>.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_INVALID_HANDLE</b></dt>
</dl>
</td>
<td width="60%">
The handle <i>hClientHandle</i>  was not found in the handle table.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_NOT_SUPPORTED</b></dt>
</dl>
</td>
<td width="60%">
This function was called from an unsupported platform. This value will be returned if this function was called from a Windows XP with SP3 or Wireless LAN API for Windows XP with SP2 client.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>RPC_STATUS</b></dt>
</dl>
</td>
<td width="60%">
Various error codes.

</td>
</tr>
</table>
 




## -remarks



The caller is responsible for calling the <a href="https://msdn.microsoft.com/241afb9d-8b16-4d76-b311-302b5492853e">WlanFreeMemory</a> function to free the memory allocated to <i>ppCapability</i>.



