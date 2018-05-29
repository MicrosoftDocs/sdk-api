---
UID: NF:dhcpcsdk.DhcpUndoRequestParams
title: DhcpUndoRequestParams function
author: windows-sdk-content
description: The DhcpUndoRequestParams function removes persistent requests previously made with a DhcpRequestParams function call.
old-location: dhcp\dhcpundorequestparams.htm
old-project: DHCP
ms.assetid: a70fc72e-0fbd-4ee7-ae87-780fdc942384
ms.author: windowssdkdev
ms.date: 05/17/2018
ms.keywords: DhcpUndoRequestParams, DhcpUndoRequestParams function [DHCP], _dhcp_dhcpundorequestparams, dhcp.dhcpundorequestparams, dhcpcsdk/DhcpUndoRequestParams
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: dhcpcsdk.h
req.include-header: 
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
req.typenames: KSJACK_DESCRIPTION, *PKSJACK_DESCRIPTION
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Dhcpcsvc.dll
api_name:
-	DhcpUndoRequestParams
product: Windows
targetos: Windows
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
---

# DhcpUndoRequestParams function


## -description


The 
<b>DhcpUndoRequestParams</b> function removes persistent requests previously made with a 
<b>DhcpRequestParams</b> function call.


## -parameters




### -param Flags [in]

Reserved. Must be zero.


### -param Reserved [in]

Reserved for future use. Must be set to <b>NULL</b>.


### -param AdapterName [in]

Name of the adapter for which information is no longer required.  Must be under 256 characters.

<div class="alert"><b>Note</b>  This parameter is no longer used.</div>
<div> </div>

### -param RequestIdStr [in]

Application identifier (ID) originally used to make a persistent request. This string must match the <i>RequestIdStr</i> parameter used in the 
<b>DhcpRequestParams</b> function call that obtained the corresponding persistent request. Note that this must match the previous application identifier (ID) used, and must be a printable string with no special characters (commas, backslashes, colons, or other illegal characters may not be used).


## -returns



Returns ERROR_SUCCESS upon successful completion. Otherwise, returns a Windows error code.




## -remarks



Persistent requests are typically made by the setup or installer process associated with the application. When appropriate, the setup or installer process would likely make the 
<b>DhcpUndoRequestParams</b> function call to cancel its associated persistent request.




## -see-also




<a href="https://msdn.microsoft.com/ca859a72-51d3-4bd5-96b9-7a9a2df95595">DHCP Functions</a>



<a href="https://msdn.microsoft.com/b4bc8b02-63b4-4751-a963-25336e8ae426">DhcpCApiInitialize</a>



<a href="https://msdn.microsoft.com/5fcbd1d9-8170-4c2b-ac98-6c04107c46e7">DhcpRequestParams</a>
 

 

