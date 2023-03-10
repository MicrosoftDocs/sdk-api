---
UID: NF:tbs.Tbsi_Get_OwnerAuth
title: Tbsi_Get_OwnerAuth function (tbs.h)
description: Retrieves the owner authorization of the TPM if the information is available in the local registry.
helpviewer_keywords: ["TBS_OWNERAUTH_TYPE_ADMIN","TBS_OWNERAUTH_TYPE_ENDORSEMENT","TBS_OWNERAUTH_TYPE_ENDORSEMENT_20","TBS_OWNERAUTH_TYPE_FULL","TBS_OWNERAUTH_TYPE_STORAGE_20","TBS_OWNERAUTH_TYPE_USER","Tbsi_Get_OwnerAuth","Tbsi_Get_OwnerAuth function [TBS]","tbs.tbsi_get_ownerauth","tbs/Tbsi_Get_OwnerAuth"]
old-location: tbs\tbsi_get_ownerauth.htm
tech.root: TBS
ms.assetid: 9D265AD2-F992-4756-9A2D-03DADB69C7DC
ms.date: 12/05/2018
ms.keywords: TBS_OWNERAUTH_TYPE_ADMIN, TBS_OWNERAUTH_TYPE_ENDORSEMENT, TBS_OWNERAUTH_TYPE_ENDORSEMENT_20, TBS_OWNERAUTH_TYPE_FULL, TBS_OWNERAUTH_TYPE_STORAGE_20, TBS_OWNERAUTH_TYPE_USER, Tbsi_Get_OwnerAuth, Tbsi_Get_OwnerAuth function [TBS], tbs.tbsi_get_ownerauth, tbs/Tbsi_Get_OwnerAuth
req.header: tbs.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
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
req.lib: Tbs.lib
req.dll: Tbs.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - Tbsi_Get_OwnerAuth
 - tbs/Tbsi_Get_OwnerAuth
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - DllExport
api_location:
 - Tbs.dll
api_name:
 - Tbsi_Get_OwnerAuth
---

# Tbsi_Get_OwnerAuth function


## -description

Retrieves the owner authorization  of the TPM if the information is available in the local registry.

## -parameters

### -param hContext [in]

TBS handle obtained from a previous call to the <a href="/windows/desktop/api/tbs/nf-tbs-tbsi_context_create">Tbsi_Context_Create</a> function.

### -param ownerauthType [in]

Unsigned 32-bit integer indicating the type of owner authentication.

<table>
<tr>
<th>Value</th>
<th>Meaning</th>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_FULL"></a><a id="tbs_ownerauth_type_full"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_FULL</b></dt>
<dt>1</dt>
</dl>
</td>
<td width="60%">
	The owner authorization is full.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_ADMIN"></a><a id="tbs_ownerauth_type_admin"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_ADMIN</b></dt>
<dt>2</dt>
</dl>
</td>
<td width="60%">
<b>Note</b>  TPM 1.2 only

The owner authorization is an administrator.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_USER"></a><a id="tbs_ownerauth_type_user"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_USER</b></dt>
<dt>3</dt>
</dl>
</td>
<td width="60%">
<b>Note</b>  TPM 1.2 only

The owner authorization is a user.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_ENDORSEMENT"></a><a id="tbs_ownerauth_type_endorsement"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_ENDORSEMENT</b></dt>
<dt>4</dt>
</dl>
</td>
<td width="60%">
<b>Note</b>  TPM 1.2 only

The owner authorization is an endorsement authorization.

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_ENDORSEMENT_20_"></a><a id="tbs_ownerauth_type_endorsement_20_"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_ENDORSEMENT_20 </b></dt>
<dt>12</dt>
</dl>
</td>
<td width="60%">
<b>Note</b>  TPM 2.0 and later

The owner authorization is an endorsement authorization. 

</td>
</tr>
<tr>
<td width="40%"><a id="TBS_OWNERAUTH_TYPE_STORAGE_20_"></a><a id="tbs_ownerauth_type_storage_20_"></a><dl>
<dt><b>TBS_OWNERAUTH_TYPE_STORAGE_20 </b></dt>
<dt>13</dt>
</dl>
</td>
<td width="60%">
<b>Note</b>  TPM 2.0 and later

The owner authorization is an administrator.

</td>
</tr>
</table>

### -param pOutputBuf [out, optional]

A pointer to a buffer to receive the TPM owner authorization information.

### -param pOutputBufLen [in, out]

An integer that, on input, specifies the size, in bytes, of the output buffer. On successful return, this value is set to the actual size of the TPM ownerAuth, in bytes.

## -returns

If the function succeeds, the function returns <b>TBS_SUCCESS</b>.

If the function fails, it returns a TBS return code that indicates the error.

<table>
<tr>
<th>Return code/value</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_SUCCESS</b></dt>
<dt>0 (0x0)</dt>
</dl>
</td>
<td width="60%">
The function was successful.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_OWNERAUTH_NOT_FOUND</b></dt>
<dt>2150121493 (0x80284015)</dt>
</dl>
</td>
<td width="60%">
The requested TPM ownerAuth value was not found.

</td>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>TBS_E_BAD_PARAMETER</b></dt>
<dt>2150121474 (0x80284002)</dt>
</dl>
</td>
<td width="60%">
The requested TPM ownerAuth value does not match the TPM version.

</td>
</tr>
</table>

## -remarks

There are additional authorization values, also known as delegation blobs, derived from the full TPM ownerAuth that allow a subset of the TPM functionality to be executed. The administrator can configure the level of ownerAuth that should be locally stored in the registry through Group Policy and the same can be obtained from this API call.

If Active Directory backup of ownerAuth is enabled through Group Policy, the default level of ownerAuth is set as Delegated which means that the full owner auth is removed from the local registry and stored in Active Directory. Only delegation blobs are locally stored in the registry in that case. Although, the level of ownerAuth storage can be explicitly configured to Full resulting in the TPM ownerAuth being locally available in the registry.