---
UID: NF:fhcfg.IFhConfigMgr.GetLocalPolicy
title: IFhConfigMgr::GetLocalPolicy (fhcfg.h)
description: Retrieves the numeric parameter for a local policy for the File History feature.
helpviewer_keywords: ["FhConfigMgr class [Windows API]","GetLocalPolicy method","GetLocalPolicy","GetLocalPolicy method [Windows API]","GetLocalPolicy method [Windows API]","FhConfigMgr class","GetLocalPolicy method [Windows API]","IFhConfigMgr interface","IFhConfigMgr interface [Windows API]","GetLocalPolicy method","IFhConfigMgr.GetLocalPolicy","IFhConfigMgr::GetLocalPolicy","fhcfg/IFhConfigMgr::GetLocalPolicy","winprog.ifhconfigmgr_getlocalpolicy"]
old-location: winprog\ifhconfigmgr_getlocalpolicy.htm
tech.root: winprog
ms.assetid: 380B77C3-CA93-48D6-9915-FB788CF24C99
ms.date: 12/05/2018
ms.keywords: FhConfigMgr class [Windows API],GetLocalPolicy method, GetLocalPolicy, GetLocalPolicy method [Windows API], GetLocalPolicy method [Windows API],FhConfigMgr class, GetLocalPolicy method [Windows API],IFhConfigMgr interface, IFhConfigMgr interface [Windows API],GetLocalPolicy method, IFhConfigMgr.GetLocalPolicy, IFhConfigMgr::GetLocalPolicy, fhcfg/IFhConfigMgr::GetLocalPolicy, winprog.ifhconfigmgr_getlocalpolicy
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
 - IFhConfigMgr::GetLocalPolicy
 - fhcfg/IFhConfigMgr::GetLocalPolicy
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
 - IFhConfigMgr.GetLocalPolicy
 - FhConfigMgr.GetLocalPolicy
---

# IFhConfigMgr::GetLocalPolicy


## -description

Retrieves the numeric parameter for a local policy for the File History feature.

> [!NOTE] 
> **IFhConfigMgr** is deprecated and may be altered or unavailable in future releases.

## -parameters

### -param LocalPolicyType [in]

Specifies the local policy.

### -param PolicyValue [out]

Receives the value of the numeric parameter for the specified local policy.

## -returns

<b>S_OK</b> on success, or an unsuccessful <b>HRESULT</b> value on failure. Possible unsuccessful <b>HRESULT</b> values include values defined in the FhErrors.h header file.

## -remarks

Each local policy contains a numeric parameter that specifies how or when the File History feature backs up files and folders. See the <a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_local_policy_type">FH_LOCAL_POLICY_TYPE</a> enumeration for more information about the local policies that can be specified.

To set the numeric parameter value for a local policy, use the <a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a> method.

## -see-also

<a href="/windows/desktop/api/fhcfg/ne-fhcfg-fh_local_policy_type">FH_LOCAL_POLICY_TYPE</a>



<a href="/windows/desktop/DevNotes/fhconfigmgr">FhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nn-fhcfg-ifhconfigmgr">IFhConfigMgr</a>



<a href="/windows/desktop/api/fhcfg/nf-fhcfg-ifhconfigmgr-setlocalpolicy">IFhConfigMgr::SetLocalPolicy</a>