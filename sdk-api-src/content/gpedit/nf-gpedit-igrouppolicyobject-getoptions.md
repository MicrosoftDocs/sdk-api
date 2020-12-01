---
UID: NF:gpedit.IGroupPolicyObject.GetOptions
title: IGroupPolicyObject::GetOptions (gpedit.h)
description: The GetOptions method retrieves the options for the GPO.
helpviewer_keywords: ["GPO_OPTION_DISABLE_MACHINE","GPO_OPTION_DISABLE_USER","GetOptions","GetOptions method [Group Policy]","GetOptions method [Group Policy]","IGroupPolicyObject interface","IGroupPolicyObject interface [Group Policy]","GetOptions method","IGroupPolicyObject.GetOptions","IGroupPolicyObject::GetOptions","_win32_igrouppolicyobject_getoptions","gpedit/IGroupPolicyObject::GetOptions","policy.igrouppolicyobject_getoptions"]
old-location: policy\igrouppolicyobject_getoptions.htm
tech.root: Policy
ms.assetid: a4b86196-04c8-4ec1-bf26-2a33e44020d2
ms.date: 12/05/2018
ms.keywords: GPO_OPTION_DISABLE_MACHINE, GPO_OPTION_DISABLE_USER, GetOptions, GetOptions method [Group Policy], GetOptions method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetOptions method, IGroupPolicyObject.GetOptions, IGroupPolicyObject::GetOptions, _win32_igrouppolicyobject_getoptions, gpedit/IGroupPolicyObject::GetOptions, policy.igrouppolicyobject_getoptions
req.header: gpedit.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista
req.target-min-winversvr: Windows Server 2008
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
req.dll: Gpedit.dll
req.irql: 
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
f1_keywords:
 - IGroupPolicyObject::GetOptions
 - gpedit/IGroupPolicyObject::GetOptions
dev_langs:
 - c++
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetOptions
---

# IGroupPolicyObject::GetOptions


## -description

The
    <b>GetOptions</b> method retrieves the options for the GPO.

## -parameters

### -param dwOptions [out]

Receives the options. This parameter can be one or more of the following options.



#### GPO_OPTION_DISABLE_USER

The user portion of the GPO is disabled.



#### GPO_OPTION_DISABLE_MACHINE

The computer portion of the GPO is disabled.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To set the options for a GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setoptions">SetOptions</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-setoptions">SetOptions</a>