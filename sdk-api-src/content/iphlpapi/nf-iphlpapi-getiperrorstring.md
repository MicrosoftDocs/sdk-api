---
UID: NF:iphlpapi.GetIpErrorString
title: GetIpErrorString function
author: windows-driver-content
description: The GetIpErrorString function retrieves an IP Helper error string.
old-location: iphlp\getiperrorstring.htm
old-project: IpHlp
ms.assetid: 4f71777a-2e87-4411-89fd-12c165d4d8ae
ms.author: windowsdriverdev
ms.date: 5/3/2018
ms.keywords: GetIpErrorString, GetIpErrorString function [IP Helper], iphlp.getiperrorstring, iphlpapi/GetIpErrorString
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
req.header: iphlpapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows XP [desktop apps only]
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
req.typenames: NET_ADDRESS_FORMAT
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Iphlpapi.dll
api_name:
-	GetIpErrorString
product: Windows
targetos: Windows
req.lib: Iphlpapi.lib
req.dll: Iphlpapi.dll
req.irql: 
req.product: GDI+ 1.1
---

# GetIpErrorString function


## -description


The <b>GetIpErrorString</b> function retrieves an IP Helper error string.


## -parameters




### -param ErrorCode [in]

The error code to be retrieved. The possible values for this parameter are defined in the <i>Ipexport.h</i> header file. 


### -param Buffer [out]

A pointer to the buffer that contains the error code string if the function returns with NO_ERROR.


### -param Size [in, out]

A pointer to a <b>DWORD</b> that specifies the length, in bytes, of the buffer pointed to by <i>Buffer</i> parameter.


## -returns



Returns NO_ERROR upon success.

If the function fails, use <a href="https://msdn.microsoft.com/b9d61342-4bcf-42e9-96f1-a5993dfb6c0c">FormatMessage</a> to obtain the message string for the returned error.




## -remarks



The <b>GetIpErrorString</b>
function can be used to retrieve an IP Helper error string for an IP error code. The <b>IP_STATUS</b> error code passed in the <i>ErrorCode</i> parameter is returned in the <b>Status</b> member of the <a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>, <a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a>, and  <a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a> structures used by the ICMP and ICMPv6 functions.   The functions that use these structures include <a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>, <a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>, <a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>, 
			<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a>, <a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>, and <a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>.

The syntax for the <b>GetIpErrorString</b>
function was slightly changed on the Microsoft Windows Software Development Kit (SDK) released for Windows Vista and later. The data type for the <i>Buffer</i> parameter was changed from <b>PWCHAR</b> to <b>PWSTR</b>. 




## -see-also




<a href="https://msdn.microsoft.com/8ea4ce42-6164-4b8e-9e79-524f456c8d09">ICMPV6_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/e6d43c35-1009-4df1-bc39-aec97178cae6">ICMP_ECHO_REPLY</a>



<a href="https://msdn.microsoft.com/4a84f29c-31bd-453c-b215-300cc782595f">ICMP_ECHO_REPLY32</a>



<a href="https://msdn.microsoft.com/2de88e92-5fa5-4d8d-9448-67a33bf02f05">IP Helper Function Reference</a>



<a href="https://msdn.microsoft.com/4896a9f8-0486-4380-bf49-d1c9ef114acc">IP Helper Start Page</a>



<a href="https://msdn.microsoft.com/b4d63ffd-37ad-4901-b017-205fb15381e7">Icmp6ParseReplies</a>



<a href="https://msdn.microsoft.com/622c769b-ede8-4bc2-ac54-98de47ae1fed">Icmp6SendEcho2</a>



<a href="https://msdn.microsoft.com/ec7c2a5f-5406-4350-b795-6e72fe25f62d">IcmpParseReplies</a>



<a href="https://msdn.microsoft.com/c3cdc535-2c13-48c6-9ab1-88cc5e5119b5">IcmpSendEcho</a>



<a href="https://msdn.microsoft.com/1f70b6cc-9085-4eb8-b2cc-3b3d98d0ea46">IcmpSendEcho2</a>



<a href="https://msdn.microsoft.com/7b2b2cae-650f-4ecb-aa2e-a55ee4026999">IcmpSendEcho2Ex</a>
 

 

