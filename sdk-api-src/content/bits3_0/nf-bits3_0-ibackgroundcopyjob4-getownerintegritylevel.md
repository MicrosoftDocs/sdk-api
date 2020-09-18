---
UID: NF:bits3_0.IBackgroundCopyJob4.GetOwnerIntegrityLevel
title: IBackgroundCopyJob4::GetOwnerIntegrityLevel (bits3_0.h)
description: Gets the integrity level of the token of the owner that created or took ownership of the job.
helpviewer_keywords: ["GetOwnerIntegrityLevel","GetOwnerIntegrityLevel method [BITS]","GetOwnerIntegrityLevel method [BITS]","IBackgroundCopyJob4 interface","IBackgroundCopyJob4 interface [BITS]","GetOwnerIntegrityLevel method","IBackgroundCopyJob4.GetOwnerIntegrityLevel","IBackgroundCopyJob4::GetOwnerIntegrityLevel","bits.ibackgroundcopyjob4_getownerintegritylevel","bits3_0/IBackgroundCopyJob4::GetOwnerIntegrityLevel"]
old-location: bits\ibackgroundcopyjob4_getownerintegritylevel.htm
tech.root: Bits
ms.assetid: 1f5d9576-0948-429b-b136-1b02d7197fcc
ms.date: 12/05/2018
ms.keywords: GetOwnerIntegrityLevel, GetOwnerIntegrityLevel method [BITS], GetOwnerIntegrityLevel method [BITS],IBackgroundCopyJob4 interface, IBackgroundCopyJob4 interface [BITS],GetOwnerIntegrityLevel method, IBackgroundCopyJob4.GetOwnerIntegrityLevel, IBackgroundCopyJob4::GetOwnerIntegrityLevel, bits.ibackgroundcopyjob4_getownerintegritylevel, bits3_0/IBackgroundCopyJob4::GetOwnerIntegrityLevel
req.header: bits3_0.h
req.include-header: Bits.h
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Bits3_0.idl
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Bits.lib
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IBackgroundCopyJob4::GetOwnerIntegrityLevel
 - bits3_0/IBackgroundCopyJob4::GetOwnerIntegrityLevel
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Bits.lib
 - Bits.dll
api_name:
 - IBackgroundCopyJob4.GetOwnerIntegrityLevel
---

# IBackgroundCopyJob4::GetOwnerIntegrityLevel


## -description

Gets the integrity level of the token of the owner that created or took ownership of the job.

## -parameters

### -param pLevel [out]

Integrity level of the token of the owner that created or took ownership of the job.

## -returns

The method returns the following return values.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>S_OK</b></dt>
</dl>
</td>
<td width="60%">
Success

</td>
</tr>
</table>

## -remarks

For details on how the integrity level of the user's token affects a job, see <a href="/windows/desktop/Bits/user-account-control-and-bits">User Account Control and BITS</a>.

This method returns the value from the <a href="/windows/desktop/api/securitybaseapi/nf-securitybaseapi-getsidsubauthority">GetSidSubAuthority</a> function. For possible mandatory integrity RID values, see <a href="/windows/desktop/SecAuthZ/well-known-sids">Well-known SIDs</a> in the Security documentation.

## -see-also

<a href="/windows/desktop/api/bits3_0/nn-bits3_0-ibackgroundcopyjob4">IBackgroundCopyJob4</a>