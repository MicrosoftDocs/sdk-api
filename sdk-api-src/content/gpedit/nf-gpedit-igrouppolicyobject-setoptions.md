---
UID: NF:gpedit.IGroupPolicyObject.SetOptions
title: IGroupPolicyObject::SetOptions (gpedit.h)
description: The SetOptions method sets the options for the GPO.
helpviewer_keywords: ["GPO_OPTION_DISABLE_MACHINE","GPO_OPTION_DISABLE_USER","IGroupPolicyObject interface [Group Policy]","SetOptions method","IGroupPolicyObject.SetOptions","IGroupPolicyObject::SetOptions","SetOptions","SetOptions method [Group Policy]","SetOptions method [Group Policy]","IGroupPolicyObject interface","_win32_igrouppolicyobject_setoptions","gpedit/IGroupPolicyObject::SetOptions","policy.igrouppolicyobject_setoptions"]
old-location: policy\igrouppolicyobject_setoptions.htm
tech.root: Policy
ms.assetid: 4caed430-2861-49cb-9418-b12bf1c46707
ms.date: 12/05/2018
ms.keywords: GPO_OPTION_DISABLE_MACHINE, GPO_OPTION_DISABLE_USER, IGroupPolicyObject interface [Group Policy],SetOptions method, IGroupPolicyObject.SetOptions, IGroupPolicyObject::SetOptions, SetOptions, SetOptions method [Group Policy], SetOptions method [Group Policy],IGroupPolicyObject interface, _win32_igrouppolicyobject_setoptions, gpedit/IGroupPolicyObject::SetOptions, policy.igrouppolicyobject_setoptions
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
 - IGroupPolicyObject::SetOptions
 - gpedit/IGroupPolicyObject::SetOptions
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
 - IGroupPolicyObject.SetOptions
---

# IGroupPolicyObject::SetOptions


## -description

The
    <b>SetOptions</b> method sets the options for the GPO.

## -parameters

### -param dwOptions [in]

Specifies the new option values. This parameter can be one or more of the following options. For more information, see the following Remarks section.



#### GPO_OPTION_DISABLE_USER

Disable the user portion of the GPO.



#### GPO_OPTION_DISABLE_MACHINE

Disable the computer portion of the GPO.

### -param dwMask [in]

Specifies the options to change. This parameter can be one or more of the following options. For more information, see the following Remarks section.



#### GPO_OPTION_DISABLE_USER

Disable the user portion of the GPO.



#### GPO_OPTION_DISABLE_MACHINE

Disable the computer portion of the GPO.

## -returns

If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.

## -remarks

<div class="alert"><b>Note</b>  A policy refresh will be automatically triggered when the user or computer portion of the local Group Policy object is enabled or disabled using the  <b>SetOptions</b> method.</div>
<div> </div>
To change an option, you must set the appropriate flag in the <i>dwMask</i> parameter. If the flag is set, then the system reads the <i>dwOptions</i> parameter to set the new state. For example, to disable the user portion of a GPO, and leave the computer portion unchanged, call the 
<b>SetOptions</b> method as follows:


```cpp
SetOptions(GPO_OPTION_DISABLE_USER, GPO_OPTION_DISABLE_USER)
```


To enable the user portion and disable the computer portion, call the 
<b>SetOptions</b> method as follows:


```cpp
SetOptions(GPO_OPTION_DISABLE_MACHINE, GPO_OPTION_DISABLE_USER | GPO_OPTION_DISABLE_MACHINE)
```


To retrieve the options for a GPO, you can call the 
<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getoptions">GetOptions</a> method.

## -see-also

<a href="/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igrouppolicyobject-getoptions">GetOptions</a>



<a href="/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igrouppolicyobject">IGroupPolicyObject</a>