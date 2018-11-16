---
UID: NF:azroles.IAzApplication.AddDelegatedPolicyUser
title: IAzApplication::AddDelegatedPolicyUser
author: windows-sdk-content
description: Adds the specified security identifier (SID) in text form to the list of principals that act as delegated policy users.
old-location: security\iazapplication_adddelegatedpolicyuser.htm
tech.root: SecAuthZ
ms.assetid: 89c0e1b9-cf51-4f4f-b530-7982645a9d14
ms.author: windowssdkdev
ms.date: 11/15/2018
ms.keywords: AddDelegatedPolicyUser, AddDelegatedPolicyUser method [Security], AddDelegatedPolicyUser method [Security],AzApplication object, AddDelegatedPolicyUser method [Security],IAzApplication interface, AzApplication object [Security],AddDelegatedPolicyUser method, IAzApplication interface [Security],AddDelegatedPolicyUser method, IAzApplication.AddDelegatedPolicyUser, IAzApplication::AddDelegatedPolicyUser, azroles/IAzApplication::AddDelegatedPolicyUser, security.iazapplication_adddelegatedpolicyuser
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
req.header: azroles.h
req.include-header: 
req.target-type: Windows
req.target-min-winverclnt: Windows Vista [desktop apps only]
req.target-min-winversvr: Windows Server 2003 [desktop apps only]
req.kmdf-ver: 
req.umdf-ver: 
req.ddi-compliance: 
req.unicode-ansi: 
req.idl: 
req.max-support: 
req.namespace: 
req.assembly: 
req.type-library: 
req.lib: Azroles.lib
req.dll: Azroles.dll
req.irql: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Azroles.dll
api_name:
 - IAzApplication.AddDelegatedPolicyUser
 - AzApplication.AddDelegatedPolicyUser
product: Windows
targetos: Windows
req.typenames: 
req.redist: Windows Server 2003 Administration Tools Pack on Windows XP
- apiref
: 
- COM
: 
- azroles.h
: 
- IAzApplication.AddDelegatedPolicyUser
: 
---

# IAzApplication::AddDelegatedPolicyUser


## -description


The <b>AddDelegatedPolicyUser</b> method adds the specified <a href="https://msdn.microsoft.com/3e9d7672-2314-45c8-8178-5a0afcfd0c50">security identifier</a> (SID) in text form to the list of principals that act as delegated policy users.


## -parameters




### -param bstrDelegatedPolicyUser [in]

Text form of the SID to add to the list of delegated policy users.


### -param varReserved [in, optional]

Reserved for future use.  This parameter can be any of the following values:

<ul>
<li>varReserved.vt == VT_ERROR and varReserved.scode == DISP_E_PARAMNOTFOUND</li>
<li>varReserved.vt == VT_EMPTY</li>
<li>varReserved.vt == VT_NULL</li>
<li>varReserved.vt == VT_I4 and varReserved.lVal == 0</li>
<li>varReserved.vt == VT_I2 and varReserved.iVal == 0</li>
</ul>

## -returns



<h3>C++</h3>
 If the method succeeds, the method returns S_OK.

An attempt to call this method on an XML store will return E_INVALIDARG.

Any other <b>HRESULT</b> value indicates that the operation failed.

<h3>VB</h3>
 If the method succeeds, the method returns S_OK.

An attempt to call this method on an XML store will return E_INVALIDARG.

Any other <b>HRESULT</b> value indicates that the operation failed.




## -remarks



Delegated policy users are principals that are allowed to read the subset of the policy data that the policy administrator of an <a href="https://msdn.microsoft.com/ea4a8a84-5003-44da-b75e-34da6bd898dd">IAzApplication</a> object uses to administer the delegated object.

<div class="alert"><b>Note</b>  Delegated policy users are not supported for XML stores.</div>
<div> </div>
To view the list of delegated policy users, use the <a href="https://msdn.microsoft.com/b20e1d5c-b07e-4f75-8b63-38036b07b24d">DelegatedPolicyUsers</a> property.

You must call the <a href="https://msdn.microsoft.com/d00d55a1-884f-46c2-b80b-f90ce8f5c648">Submit</a> method to persist any changes made by this method.



