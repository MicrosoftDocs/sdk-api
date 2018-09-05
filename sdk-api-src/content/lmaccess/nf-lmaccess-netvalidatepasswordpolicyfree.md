---
UID: NF:lmaccess.NetValidatePasswordPolicyFree
title: NetValidatePasswordPolicyFree function
author: windows-sdk-content
description: The NetValidatePasswordPolicyFree function frees the memory that the NetValidatePasswordPolicy function allocates for the OutputArg parameter, which is a NET_VALIDATE_OUTPUT_ARG structure.
old-location: netmgmt\netvalidatepasswordpolicyfree.htm
old-project: netmgmt
ms.assetid: 263834cd-a0e2-4ec0-9cb1-c03eb198de3a
ms.author: windowssdkdev
ms.date: 08/29/2018
ms.keywords: NetValidatePasswordPolicyFree, NetValidatePasswordPolicyFree function [Network Management], lmaccess/NetValidatePasswordPolicyFree, netmgmt.netvalidatepasswordpolicyfree
ms.prod: windows
ms.technology: windows-sdk
ms.topic: function
req.header: lmaccess.h
req.include-header: Lm.h
req.redist: 
req.target-type: Windows
req.target-min-winverclnt: None supported
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
tech.root: 
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetValidatePasswordPolicyFree
product: Windows
targetos: Windows
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
---

# NetValidatePasswordPolicyFree function


## -description


The <b>NetValidatePasswordPolicyFree</b> function frees the memory that the <a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a> function allocates for the <i>OutputArg</i> parameter, which is a <a href="https://msdn.microsoft.com/833c89c3-34ba-485b-a310-1d709aa618cd">NET_VALIDATE_OUTPUT_ARG</a> structure.


## -parameters




### -param OutputArg [in]

Pointer to the memory allocated for the <i>OutputArg</i> parameter by a call to the <b>NetValidatePasswordPolicy</b> function.


## -returns



If the function frees the memory, or if there is no memory to free from a previous call to <b>NetValidatePasswordPolicy</b>, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see <a href="https://msdn.microsoft.com/4a3a8feb-a05f-4614-8f04-1f507da7e5b7">System Error Codes</a>. 





## -remarks



No special group membership is required to successfully execute this function.




## -see-also




<a href="https://msdn.microsoft.com/be5ce51b-6568-49c8-954d-7b0d4bcb8611">NetValidatePasswordPolicy</a>



<a href="https://msdn.microsoft.com/dd159e2e-f37e-46b2-b980-008b73d40b39">Network
		  Management Functions</a>



<a href="https://msdn.microsoft.com/426c7b2e-027c-4a88-97b7-eba5201d0f0d">Network Management
		  Overview</a>
 

 

