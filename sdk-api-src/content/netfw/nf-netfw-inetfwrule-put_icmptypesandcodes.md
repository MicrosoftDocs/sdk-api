---
UID: NF:netfw.INetFwRule.put_IcmpTypesAndCodes
title: INetFwRule::put_IcmpTypesAndCodes
author: windows-sdk-content
description: Specifies the list of ICMP types and codes for this rule.
old-location: ics\inetfwrule_icmptypesandcodes.htm
tech.root: ics
ms.assetid: 5b1e2e50-7ca1-4a96-a1c3-1f55f51a6a4f
ms.author: windowssdkdev
ms.date: 12/5/2018
ms.keywords: INetFwRule interface [ICS/ICF],IcmpTypesAndCodes property, INetFwRule.IcmpTypesAndCodes, INetFwRule.put_IcmpTypesAndCodes, INetFwRule::IcmpTypesAndCodes, INetFwRule::get_IcmpTypesAndCodes, INetFwRule::put_IcmpTypesAndCodes, IcmpTypesAndCodes property [ICS/ICF], IcmpTypesAndCodes property [ICS/ICF],INetFwRule interface, ics.inetfwrule_icmptypesandcodes, netfw/INetFwRule::IcmpTypesAndCodes, netfw/INetFwRule::get_IcmpTypesAndCodes, netfw/INetFwRule::put_IcmpTypesAndCodes, put_IcmpTypesAndCodes
ms.topic: method
req.header: netfw.h
req.include-header: 
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
req.lib: 
req.dll: FirewallAPI.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - FirewallAPI.dll
api_name:
 - INetFwRule.IcmpTypesAndCodes
 - INetFwRule.get_IcmpTypesAndCodes
 - INetFwRule.put_IcmpTypesAndCodes
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# INetFwRule::put_IcmpTypesAndCodes


## -description


Specifies the list of ICMP types and codes for this rule.

This property is read/write.


## -parameters


## -remarks



This property is optional.

Also see the restrictions on changing properties described in the Remarks section of the <a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a> interface page.

The <i>icmpTypesAndCodes</i> parameter is a list of ICMP types and codes     separated by semicolon. "*" indicates all ICMP types and codes.




## -see-also




<a href="https://msdn.microsoft.com/59e2a140-bf55-4f0e-bf4b-1a39d3dc0457">INetFwRule</a>
 

 

