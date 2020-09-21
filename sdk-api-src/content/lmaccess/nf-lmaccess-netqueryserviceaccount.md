---
UID: NF:lmaccess.NetQueryServiceAccount
title: NetQueryServiceAccount function (lmaccess.h)
description: Gets information about the specified managed service account.
helpviewer_keywords: ["NetQueryServiceAccount","NetQueryServiceAccount function [Security]","lmaccess/NetQueryServiceAccount","security.netqueryserviceaccount"]
old-location: security\netqueryserviceaccount.htm
tech.root: security
ms.assetid: ee253cab-bd53-426e-809a-12a1ccdc010b
ms.date: 12/05/2018
ms.keywords: NetQueryServiceAccount, NetQueryServiceAccount function [Security], lmaccess/NetQueryServiceAccount, security.netqueryserviceaccount
req.header: lmaccess.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 7 [desktop apps only]
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
req.lib: 
req.dll: Netapi32.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - NetQueryServiceAccount
 - lmaccess/NetQueryServiceAccount
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Netapi32.dll
api_name:
 - NetQueryServiceAccount
---

# NetQueryServiceAccount function


## -description

Gets information about the specified managed service account.

## -parameters

### -param ServerName [in, optional]

The value of this parameter must be <b>NULL</b>.

### -param AccountName [in]

The name of the account to be created.

### -param InfoLevel [in]

Specifies the format of the data returned in the <i>Buffer</i> parameter. This can be the following value.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt>0</dt>
</dl>
</td>
<td width="60%">
The <i>Buffer</i> parameter contains an <a href="/windows/desktop/api/lmaccess/ns-lmaccess-msa_info_0">MSA_INFO_0</a> structure.

</td>
</tr>
</table>

### -param Buffer [out]

Information about the specified service account.

When you have finished using this buffer, free it by calling the <a href="/windows/desktop/api/lmapibuf/nf-lmapibuf-netapibufferfree">NetApiBufferFree</a> function.

## -returns

If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.

## -see-also

<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netaddserviceaccount">NetAddServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netenumerateserviceaccounts">NetEnumerateServiceAccounts</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netisserviceaccount">NetIsServiceAccount</a>



<a href="/windows/desktop/api/lmaccess/nf-lmaccess-netremoveserviceaccount">NetRemoveServiceAccount</a>