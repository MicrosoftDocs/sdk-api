---
UID: NF:dhcpsapi.DhcpEnumOptionsV5
title: DhcpEnumOptionsV5 function
author: windows-sdk-content
description: The DhcpEnumOptionsV5 function returns an enumerated list of DHCP options for a given user or vendor class.
old-location: dhcp\dhcpenumoptionsv5.htm
tech.root: DHCP
ms.assetid: 9fe14fe7-d207-4a5a-b36c-4a5ab32a6bc3
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: DHCP_FLAGS_OPTION_IS_VENDOR, DhcpEnumOptionsV5, DhcpEnumOptionsV5 function [DHCP], dhcp.dhcpenumoptionsv5, dhcpsapi/DhcpEnumOptionsV5
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2008 R2 [desktop apps only]
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
 - DhcpEnumOptionsV5
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
- apiref
: 
- 
: 
- DhcpEnumOptionsV5
: 
---

# DhcpEnumOptionsV5 function


## -description


The <b>DhcpEnumOptionsV5</b> function returns an enumerated list of DHCP options for a given user or vendor class.


## -parameters




### -param ServerIpAddress [in]

Unicode string that specifies the IP address or hostname of the DHCP server.


### -param Flags [in]

A set of flags that indicate the option definition for enumeration.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0x00000000</dt>
</dl>
</td>
<td width="60%">
The option definitions are enumerated for a default vendor class.

</td>
</tr>
<tr>
<td width="40%"><a id="DHCP_FLAGS_OPTION_IS_VENDOR"></a><a id="dhcp_flags_option_is_vendor"></a><dl>
<dt><b>DHCP_FLAGS_OPTION_IS_VENDOR</b></dt>
<dt>0x00000003</dt>
</dl>
</td>
<td width="60%">
The option definitions are enumerated for a specific vendor class.

</td>
</tr>
</table>
 


### -param ClassName [in]

Pointer to a Unicode string that contains the name of the class whose options will be enumerated. This parameter is optional. 


### -param VendorName [in]

Pointer to a Unicode string that contains the name of the vendor for the class. This parameter is optional. If a vendor class name is not provided, the default vendor class name is used.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 1000 bytes, and 2000 bytes of option definitions are stored on the server, the resume handle can be used after the first 1000 bytes are retrieved to obtain the next 1000 on a subsequent call, and so forth.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of bytes of options to return. If the number of remaining unenumerated option definitions (in bytes) is less than this value, all option definitions are returned.


### -param Options [out]

Pointer to a <a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a> structure containing the returned option definitions. If there are no option definitions available on the DHCP server, this parameter will return null.


### -param OptionsRead [out]

Pointer to a DWORD value that specifies the number of option definitions returned in <i>Options</i>.


### -param OptionsTotal [out]

Pointer to a DWORD value that specifies the total number of unenumerated option definitions on the DHCP server.


## -returns



This function returns <b>ERROR_SUCCESS</b> upon a successful call. Otherwise, it returns one of the <a href="https://msdn.microsoft.com/6370313f-d7db-4ff1-b0e0-7fa47474facb">DHCP Server Management API Error Codes</a>.

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
This call was performed by a client who is not a member of the "DHCP Administrators" security group.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>ERROR_DHCP_CLASS_NOT_FOUND</b></dt>
</dl>
</td>
<td width="60%">
The supplied user or vendor class name is either incorrect or unknown.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/15b9bab5-8211-47c8-bc93-96c922c1aec1">DHCP_OPTION_ARRAY</a>



<a href="https://msdn.microsoft.com/de6e8f87-af4b-4e7f-8468-54359c5a8907">DhcpCreateOptionV5</a>



<a href="https://msdn.microsoft.com/53b57879-7533-4e92-a179-d6786052ad46">DhcpRemoveOptionV5</a>
 

 

