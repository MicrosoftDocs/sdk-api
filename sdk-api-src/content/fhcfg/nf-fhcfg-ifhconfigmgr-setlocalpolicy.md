---
UID: NF:fhcfg.IFhConfigMgr.SetLocalPolicy
title: IFhConfigMgr::SetLocalPolicy (fhcfg.h)
description: Changes the numeric parameter value of a local policy in an FhConfigMgr object.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","SetLocalPolicy method","IFhConfigMgr interface [Windows API]","SetLocalPolicy method","IFhConfigMgr.SetLocalPolicy","IFhConfigMgr::SetLocalPolicy","SetLocalPolicy","SetLocalPolicy method [Windows API]","SetLocalPolicy method [Windows API]","FhConfigMgr class","SetLocalPolicy method [Windows API]","IFhConfigMgr interface","fhcfg/IFhConfigMgr::SetLocalPolicy","winprog.ifhconfigmgr_setlocalpolicy"]
old-location: winprog\ifhconfigmgr_setlocalpolicy.htm
tech.root: winprog
ms.assetid: A1106349-6B14-4A44-B845-7853FA1919D6
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],SetLocalPolicy method, IFhConfigMgr interface [Windows API],SetLocalPolicy method, IFhConfigMgr.SetLocalPolicy, IFhConfigMgr::SetLocalPolicy, SetLocalPolicy, SetLocalPolicy method [Windows API], SetLocalPolicy method [Windows API],FhConfigMgr class, SetLocalPolicy method [Windows API],IFhConfigMgr interface, fhcfg/IFhConfigMgr::SetLocalPolicy, winprog.ifhconfigmgr_setlocalpolicy
req.header: fhcfg.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows 8 [desktop apps only]
req.target-min-winversvr: Windows Server 2012 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: Fhcfg.idl
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
 - IFhConfigMgr::SetLocalPolicy
 - fhcfg/IFhConfigMgr::SetLocalPolicy
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Fhcfg.h
api_name:
 - IFhConfigMgr.SetLocalPolicy
 - FhConfigMgr.SetLocalPolicy
---

# IFhConfigMgr::SetLocalPolicy


## -description

Changes the numeric parameter value of a local policy in an <a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a> object.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param LocalPolicyType [in]

Specifies the local policy.

### -param PolicyValue [in]

Specifies the new value of the numeric parameter for the specified local policy.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

Each local policy contains a numeric parameter that specifies how or when the File History feature backs up files and folders. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_local_policy_type">FH_LOCAL_POLICY_TYPE</a> enumeration for more information about the local policies that can be specified.

To retrieve the numeric parameter value for a local policy, use the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">IFhConfigMgr::GetLocalPolicy</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_local_policy_type">FH_LOCAL_POLICY_TYPE</a>



<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-getlocalpolicy">IFhConfigMgr::GetLocalPolicy</a>