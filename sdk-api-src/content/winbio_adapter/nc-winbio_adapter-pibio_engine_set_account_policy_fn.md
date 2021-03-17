---
UID: NC:winbio_adapter.PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN
title: PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN (winbio_adapter.h)
description: Sets the extended default and per-user antispoofing policies used by the engine adapter.
helpviewer_keywords: ["EngineAdapterSetAccountPolicy","EngineAdapterSetAccountPolicy callback function [Windows Biometric Framework API]","PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN","PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN callback","secbiomet.engineadaptersetaccountpolicy","winbio_adapter/EngineAdapterSetAccountPolicy"]
old-location: secbiomet\engineadaptersetaccountpolicy.htm
tech.root: SecBioMet
ms.assetid: 9D2C6CF9-A069-40AD-9BB7-81797F7B2FE6
ms.date: 12/05/2018
ms.keywords: EngineAdapterSetAccountPolicy, EngineAdapterSetAccountPolicy callback function [Windows Biometric Framework API], PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN, PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN callback, secbiomet.engineadaptersetaccountpolicy, winbio_adapter/EngineAdapterSetAccountPolicy
req.header: winbio_adapter.h
req.include-header: Winbio_adapter.h
req.target-type: Windows
req.target-min-winverclnt: Windows 10 [desktop apps only]
req.target-min-winversvr: Windows Server 2016 [desktop apps only]
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
req.dll: 
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN
 - winbio_adapter/PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - UserDefined
api_location:
 - Winbio_adapter.h
api_name:
 - EngineAdapterSetAccountPolicy
---

# PIBIO_ENGINE_SET_ACCOUNT_POLICY_FN callback function


## -description

Called by the Windows Biometric Framework to set the extended default and per-user antispoofing policies used by the engine adapter.

## -parameters

### -param Pipeline [in, out]

Pointer to the <a href="/windows/desktop/api/winbio_adapter/ns-winbio_adapter-winbio_pipeline">WINBIO_PIPELINE</a> structure associated with the biometric unit performing the operation.

### -param PolicyItemArray [in]

Address of an array of <a href="/windows/desktop/SecBioMet/winbio-account-policy">WINBIO_ACCOUNT_POLICY</a> structures, which the routine should use to update the policies it is applying to any identities it detects.

### -param PolicyItemCount [in]

The number of elements in the array pointed to by the <i>PolicyItemArray</i> parameter.

## -returns

If the function succeeds, it returns <b>S_OK</b>. If the function fails, it must return one of the following <b>HRESULT</b> values to indicate the error.

<table>
<tr>
<th>Return code</th>
<th>Description</th>
</tr>
<tr>
<td width="40%">
<dl>
<dt><b>E_some_error </b></dt>
</dl>
</td>
<td width="60%">
Errors return by the method are logged but ignored.

</td>
</tr>
</table>

## -remarks

This method is called each time the biometric unit is activated.

This method executes in the context of the same thread that activated the biometric unit and that processed all other requests for the unit.

The Identity.Type field of the first element in the <i>PolicyItemArray</i> will always be <b>WINBIO_ID_TYPE_WILDCARD</b>. This indicates that the policy item contains a default AntiSpoofBehavior value which should be applied to any user account that isn’t explicitly listed in the rest of the array.

If the <i>PolicyItemArray</i> contains more than one element, the Identity.Type field of the remaining items will be <b>WINBIO_ID_TYPE_WILDCARD</b>, and the Identity.Value.AccountSid.Data field will contain the SID of a user account that requires the antispoof policy behavior specified in the AntiSpoofBehavior field of the array element.