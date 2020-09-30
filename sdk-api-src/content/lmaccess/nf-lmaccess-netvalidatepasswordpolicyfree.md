---
UID: NF:lmaccess.NetValidatePasswordPolicyFree
title: NetValidatePasswordPolicyFree function (lmaccess.h)
description: The NetValidatePasswordPolicyFree function frees the memory that the NetValidatePasswordPolicy function allocates for the OutputArg parameter, which is a NET_VALIDATE_OUTPUT_ARG structure.
helpviewer_keywords: ["NetValidatePasswordPolicyFree","NetValidatePasswordPolicyFree function [Network Management]","lmaccess/NetValidatePasswordPolicyFree","netmgmt.netvalidatepasswordpolicyfree"]
old-location: netmgmt\netvalidatepasswordpolicyfree.htm
tech.root: NetMgmt
ms.assetid: 263834cd-a0e2-4ec0-9cb1-c03eb198de3a
ms.date: 12/05/2018
ms.keywords: NetValidatePasswordPolicyFree, NetValidatePasswordPolicyFree function [Network Management], lmaccess/NetValidatePasswordPolicyFree, netmgmt.netvalidatepasswordpolicyfree
req.header: lmaccess.h
req.include-header: Lm.h
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
req.lib: Netapi32.lib
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetValidatePasswordPolicyFree
 - lmaccess/NetValidatePasswordPolicyFree
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
 - samcli.dll
api_name:
 - NetValidatePasswordPolicyFree
---

# NetValidatePasswordPolicyFree function


## -description

The <b>NetValidatePasswordPolicyFree</b> function frees the memory that the <a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a> function allocates for the <i>OutputArg</i> parameter, which is a <a href="/windows/desktop/api/lmaccess/ns-lmaccess-net_validate_output_arg">NET_VALIDATE_OUTPUT_ARG</a> structure.

## -parameters

### -param OutputArg [in]

Pointer to the memory allocated for the <i>OutputArg</i> parameter by a call to the <b>NetValidatePasswordPolicy</b> function.

## -returns

If the function frees the memory, or if there is no memory to free from a previous call to <b>NetValidatePasswordPolicy</b>, the return value is NERR_Success.

If the function fails, the return value is a system error code. For a list of error codes, see <a href="/windows/desktop/Debug/system-error-codes">System Error Codes</a>.

## -remarks

No special group membership is required to successfully execute this function.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netvalidatepasswordpolicy">NetValidatePasswordPolicy</a>



<a href="/windows/desktop/NetMgmt/network-management-functions">Network
		  Management Functions</a>



<a href="/windows/desktop/NetMgmt/network-management">Network Management
		  Overview</a>