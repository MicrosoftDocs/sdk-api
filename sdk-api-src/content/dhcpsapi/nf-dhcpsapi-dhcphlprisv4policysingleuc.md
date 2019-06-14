---
UID: NF:dhcpsapi.DhcpHlprIsV4PolicySingleUC
title: DhcpHlprIsV4PolicySingleUC function (dhcpsapi.h)
author: windows-sdk-content
description: Verifies that a DHCP server policy is based on a single user class.
old-location: dhcp\dhcphlprisv4policysingleuc.htm
tech.root: DHCP
ms.assetid: 46c20727-0e7a-42cf-a571-c1198b124ed0
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: DhcpHlprIsV4PolicySingleUC, DhcpHlprIsV4PolicySingleUC function [DHCP], dhcp.dhcphlprisv4policysingleuc, dhcpsapi/DhcpHlprIsV4PolicySingleUC
ms.topic: function
req.header: dhcpsapi.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: None supported
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
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
 - DhcpHlprIsV4PolicySingleUC
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# DhcpHlprIsV4PolicySingleUC function


## -description


The <b>DhcpHlprIsV4PolicySingleUC</b> function verifies that a DHCP server policy is based on a single user class.


## -parameters




### -param Policy [in]

Pointer to a <a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/ns-dhcpsapi-_dhcp_policy">DHCP_POLICY</a> structure that contains the policy to verify.


## -returns



The API returns <b>TRUE</b> if there is a single condition associated with the specified policy. This condition should be based on one of the user classes defined on the DHCP server. Otherwise, it returns <b>FALSE</b>.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policycondition">DhcpHlprAddV4PolicyCondition</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyexpr">DhcpHlprAddV4PolicyExpr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlpraddv4policyrange">DhcpHlprAddV4PolicyRange</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprcreatev4policy">DhcpHlprCreateV4Policy</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprfreev4policy">DhcpHlprFreeV4Policy</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policyvalid">DhcpHlprIsV4PolicyValid</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprisv4policywellformed">DhcpHlprIsV4PolicyWellFormed</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprmodifyv4policyexpr">DhcpHlprModifyV4PolicyExpr</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/dhcpsapi/nf-dhcpsapi-dhcphlprresetv4policyexpr">DhcpHlprResetV4PolicyExpr</a>
 

 

