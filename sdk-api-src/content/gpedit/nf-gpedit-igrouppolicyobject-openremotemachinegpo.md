---
UID: NF:gpedit.IGroupPolicyObject.OpenRemoteMachineGPO
title: IGroupPolicyObject::OpenRemoteMachineGPO (gpedit.h)
description: The OpenRemoteMachineGPO method opens the default GPO for the specified remote computer and optionally loads the registry information.
helpviewer_keywords: ["GPO_OPEN_LOAD_REGISTRY","GPO_OPEN_READ_ONLY","IGroupPolicyObject interface [Group Policy]","OpenRemoteMachineGPO method","IGroupPolicyObject.OpenRemoteMachineGPO","IGroupPolicyObject::OpenRemoteMachineGPO","OpenRemoteMachineGPO","OpenRemoteMachineGPO method [Group Policy]","OpenRemoteMachineGPO method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_openremotemachinegpo","gpedit/IGroupPolicyObject::OpenRemoteMachineGPO","policy.igrouppolicyobject_openremotemachinegpo"]
old-location: policy\igrouppolicyobject_openremotemachinegpo.htm
tech.root: Policy
ms.assetid: ac124b48-7eb6-473b-a96b-de9b1a903f28
ms.date: 12/05/2018
ms.keywords: GPO_OPEN_LOAD_REGISTRY, GPO_OPEN_READ_ONLY, IGroupPolicyObject interface [Group Policy],OpenRemoteMachineGPO method, IGroupPolicyObject.OpenRemoteMachineGPO, IGroupPolicyObject::OpenRemoteMachineGPO, OpenRemoteMachineGPO, OpenRemoteMachineGPO method [Group Policy], OpenRemoteMachineGPO method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_openremotemachinegpo, gpedit/IGroupPolicyObject::OpenRemoteMachineGPO, policy.igrouppolicyobject_openremotemachinegpo
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
 - IGroupPolicyObject::OpenRemoteMachineGPO
 - gpedit/IGroupPolicyObject::OpenRemoteMachineGPO
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
 - IGroupPolicyObject.OpenRemoteMachineGPO
---

# IGroupPolicyObject::OpenRemoteMachineGPO


## -description

The
    <b>OpenRemoteMachineGPO</b> method opens the default GPO for the specified remote computer and optionally loads the registry information.

## -parameters

### -param pszComputerName [in]

Specifies the name of the computer. The format of the name is &#92;&#92;<i>ComputerName</i>.

### -param dwFlags [in]

Specifies whether or not the registry information should be loaded for the GPO. This parameter can be one of the following values.



#### GPO_OPEN_LOAD_REGISTRY

Load the registry information.



#### GPO_OPEN_READ_ONLY

Open the GPO in read-only mode.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

To retrieve the computer name of a remote GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getmachinename">GetMachineName</a> method. Call 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openlocalmachinegpo">OpenLocalMachineGPO</a> to open the default GPO for a local computer.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getmachinename">GetMachineName</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-openlocalmachinegpo">OpenLocalMachineGPO</a>