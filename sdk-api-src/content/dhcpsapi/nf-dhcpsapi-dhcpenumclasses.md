---
UID: NF:dhcpsapi.DhcpEnumClasses
title: DhcpEnumClasses function
author: windows-driver-content
description: Enumerates the user or vendor classes configured for the DHCP server.
old-location: dhcp\dhcpenumclasses.htm
old-project: DHCP
ms.assetid: 93f37424-1a81-477e-85da-359885e94349
ms.author: windowsdriverdev
ms.date: 5/2/2018
ms.keywords: DhcpEnumClasses, DhcpEnumClasses function [DHCP], dhcp.dhcpenumclasses, dhcpsapi/DhcpEnumClasses
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
req.typenames: QuarantineStatus
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpsapi.dll
api_name:
-	DhcpEnumClasses
product: Windows
targetos: Windows
req.lib: Dhcpsapi.lib
req.dll: Dhcpsapi.dll
req.irql: 
---

# DhcpEnumClasses function


## -description


The <b>DhcpEnumClasses</b> function enumerates the  user or vendor classes configured for the DHCP server.


## -parameters




### -param ServerIpAddress [in]

Pointer to a Unicode string that specifies the IP address or hostname of the DHCP server.


### -param ReservedMustBeZero [in]

Reserved. This field must be set to zero.


### -param ResumeHandle [in, out]

Pointer to a <a href="https://msdn.microsoft.com/8e29f488-2978-43dd-b7ba-edad2e3e4b29">DHCP_RESUME_HANDLE</a> value that identifies the enumeration operation. Initially, this value should be zero, with a successful call returning the handle value used for subsequent enumeration requests. For example, if <i>PreferredMaximum</i> is set to 100 classes, and 200 classes are stored on the server, the resume handle can be used after the first 100 classes are retrieved to obtain the next 100 on a subsequent call, and so forth.


### -param PreferredMaximum [in]

Specifies the preferred maximum number of classes to return. If the number of remaining unenumerated classes is less than this value, then that amount will be returned. To retrieve all classes available on the DHCP server, set this parameter to 0xFFFFFFFF.


### -param ClassInfoArray [out]

Pointer to a  <a href="https://msdn.microsoft.com/716beba3-cba2-406c-a41f-2f08b6a7dc5a">DHCP_CLASS_INFO_ARRAY</a> structure that contains the returned classes. If there are no classes available on the DHCP server, this parameter will return null.


### -param nRead [out]

Pointer to a DWORD value that specifies the number of classes returned in <i>ClassInfoArray</i>.


### -param nTotal [out]

Pointer to a DWORD value that specifies the total number of classes stored on the DHCP server.


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
<dt><b>ERROR_DHCP_JET_ERROR</b></dt>
</dl>
</td>
<td width="60%">
An error occurred while accessing the DHCP server's database.

</td>
</tr>
</table>
 




## -see-also




<a href="https://msdn.microsoft.com/716beba3-cba2-406c-a41f-2f08b6a7dc5a">
		  DHCP_CLASS_INFO_ARRAY</a>



<a href="https://msdn.microsoft.com/ae30baba-a2cd-4662-a62a-58b59d119dc4">DhcpCreateClass</a>



<a href="https://msdn.microsoft.com/45659805-d0d0-4b84-ac98-4a0f53133b0c">DhcpDeleteClass</a>
 

 

