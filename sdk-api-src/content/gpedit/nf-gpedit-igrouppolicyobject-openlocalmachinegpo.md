---
UID: NF:gpedit.IGroupPolicyObject.OpenLocalMachineGPO
title: IGroupPolicyObject::OpenLocalMachineGPO (gpedit.h)
description: The OpenLocalMachineGPO method opens the default GPO for the computer and optionally loads the registry information.
helpviewer_keywords: ["GPO_OPEN_LOAD_REGISTRY","GPO_OPEN_READ_ONLY","IGroupPolicyObject interface [Group Policy]","OpenLocalMachineGPO method","IGroupPolicyObject.OpenLocalMachineGPO","IGroupPolicyObject::OpenLocalMachineGPO","OpenLocalMachineGPO","OpenLocalMachineGPO method [Group Policy]","OpenLocalMachineGPO method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_openlocalmachinegpo","gpedit/IGroupPolicyObject::OpenLocalMachineGPO","policy.igrouppolicyobject_openlocalmachinegpo"]
old-location: policy\igrouppolicyobject_openlocalmachinegpo.htm
tech.root: Policy
ms.assetid: c986152b-59cd-4733-bcdd-ee7f0b6907ad
ms.date: 12/05/2018
ms.keywords: GPO_OPEN_LOAD_REGISTRY, GPO_OPEN_READ_ONLY, IGroupPolicyObject interface [Group Policy],OpenLocalMachineGPO method, IGroupPolicyObject.OpenLocalMachineGPO, IGroupPolicyObject::OpenLocalMachineGPO, OpenLocalMachineGPO, OpenLocalMachineGPO method [Group Policy], OpenLocalMachineGPO method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_openlocalmachinegpo, gpedit/IGroupPolicyObject::OpenLocalMachineGPO, policy.igrouppolicyobject_openlocalmachinegpo
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
 - IGroupPolicyObject::OpenLocalMachineGPO
 - gpedit/IGroupPolicyObject::OpenLocalMachineGPO
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
 - IGroupPolicyObject.OpenLocalMachineGPO
---

# IGroupPolicyObject::OpenLocalMachineGPO


## -description

The
    <b>OpenLocalMachineGPO</b> method opens the default GPO for the computer and optionally loads the registry information.

## -parameters

### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To open the default GPO for a remote computer, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openremotemachinegpo">OpenRemoteMachineGPO</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openremotemachinegpo">OpenRemoteMachineGPO</a>