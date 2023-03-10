---
UID: NN:gpedit.IGroupPolicyObject
title: IGroupPolicyObject (gpedit.h)
description: The IGroupPolicyObject interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.
helpviewer_keywords: ["IGroupPolicyObject","IGroupPolicyObject interface [Group Policy]","IGroupPolicyObject interface [Group Policy]","described","_win32_igrouppolicyobject","gpedit/IGroupPolicyObject","policy.igrouppolicyobject"]
old-location: policy\igrouppolicyobject.htm
tech.root: Policy
ms.assetid: b3cd31a1-c238-4eb2-8164-9c4891e6227b
ms.date: 12/05/2018
ms.keywords: IGroupPolicyObject, IGroupPolicyObject interface [Group Policy], IGroupPolicyObject interface [Group Policy],described, _win32_igrouppolicyobject, gpedit/IGroupPolicyObject, policy.igrouppolicyobject
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
 - IGroupPolicyObject
 - gpedit/IGroupPolicyObject
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
 - IGroupPolicyObject
---

# IGroupPolicyObject interface


## -description

The
    <b>IGroupPolicyObject</b> interface provides methods to create and modify a GPO directly, without using the Group Policy Object Editor.

Note that this interface does not support multithreaded object concurrency.

## -inheritance

The <b>IGroupPolicyObject</b> interface inherits from the <a href="/windows/desktop/api/unknwn/nn-unknwn-iunknown">IUnknown</a> interface. <b>IGroupPolicyObject</b> also has these types of members:

## -remarks

For methods that Microsoft Management Console (MMC) extension snap-ins can use to communicate with the Group Policy Object Editor, see the 
<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a> interface.

## -see-also

<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy Overview</a>
