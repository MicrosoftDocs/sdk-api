---
UID: NF:lmaccess.NetQueryServiceAccount
title: NetQueryServiceAccount function
author: windows-driver-content
description: Gets information about the specified managed service account.
old-location: security\netqueryserviceaccount.htm
old-project: SecMgmt
ms.assetid: ee253cab-bd53-426e-809a-12a1ccdc010b
ms.author: windowsdriverdev
ms.date: 5/9/2018
ms.keywords: NetQueryServiceAccount, NetQueryServiceAccount function [Security], lmaccess/NetQueryServiceAccount, security.netqueryserviceaccount
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: function
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
req.typenames: MSA_INFO_STATE, *PMSA_INFO_STATE
topic_type:
-	APIRef
-	kbSyntax
api_type:
-	DllExport
api_location:
-	Netapi32.dll
api_name:
-	NetQueryServiceAccount
product: Windows
targetos: Windows
req.lib: 
req.dll: Netapi32.dll
req.irql: 
req.product: GDI+ 1.1
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
The <i>Buffer</i> parameter contains an <a href="https://msdn.microsoft.com/21e04ee8-98c9-4c78-9564-e07f5edaf847">MSA_INFO_0</a> structure.

</td>
</tr>
</table>
 


### -param Buffer [out]

Information about the specified service account.

When you have finished using this buffer, free it by calling the <a href="https://msdn.microsoft.com/0e99483c-8cd7-402a-8bf6-1e0118764dd3">NetApiBufferFree</a> function.


## -returns



If the function succeeds, it returns <b>STATUS_SUCCESS</b>.

If the function fails, it returns an error code.




## -see-also




<a href="https://msdn.microsoft.com/004bd392-8837-4d98-905a-cd19ed02817d">NetAddServiceAccount</a>



<a href="https://msdn.microsoft.com/048116b6-1bae-4dcc-9bd0-a466c395e5d8">NetEnumerateServiceAccounts</a>



<a href="https://msdn.microsoft.com/975e7c0d-d803-4d78-99ed-d07369341674">NetIsServiceAccount</a>



<a href="https://msdn.microsoft.com/f67745b7-bdfd-44bc-83e0-2ad24b78e137">NetRemoveServiceAccount</a>
 

 

