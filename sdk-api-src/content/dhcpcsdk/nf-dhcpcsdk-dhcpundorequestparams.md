---
UID: NF:dhcpcsdk.DhcpUndoRequestParams
title: DhcpUndoRequestParams function (dhcpcsdk.h)
description: The DhcpUndoRequestParams function removes persistent requests previously made with a DhcpRequestParams function call.
helpviewer_keywords: ["DhcpUndoRequestParams","DhcpUndoRequestParams function [DHCP]","_dhcp_dhcpundorequestparams","dhcp.dhcpundorequestparams","dhcpcsdk/DhcpUndoRequestParams"]
old-location: dhcp\dhcpundorequestparams.htm
tech.root: DHCP
ms.assetid: a70fc72e-0fbd-4ee7-ae87-780fdc942384
ms.date: 12/05/2018
ms.keywords: DhcpUndoRequestParams, DhcpUndoRequestParams function [DHCP], _dhcp_dhcpundorequestparams, dhcp.dhcpundorequestparams, dhcpcsdk/DhcpUndoRequestParams
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
req.lib: Dhcpcsvc.lib
req.dll: Dhcpcsvc.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - DhcpUndoRequestParams
 - dhcpcsdk/DhcpUndoRequestParams
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Dhcpcsvc.dll
api_name:
 - DhcpUndoRequestParams
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

GUID of the adapter for which information is no longer required.  Must be under 256 characters.

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

<a href="/previous-versions/windows/desktop/dhcp/dhcp-functions">DHCP Functions</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcpcapiinitialize">DhcpCApiInitialize</a>



<a href="/previous-versions/windows/desktop/api/dhcpcsdk/nf-dhcpcsdk-dhcprequestparams">DhcpRequestParams</a>