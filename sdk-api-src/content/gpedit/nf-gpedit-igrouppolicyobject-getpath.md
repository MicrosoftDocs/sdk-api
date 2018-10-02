---
UID: NF:gpedit.IGroupPolicyObject.GetPath
title: IGroupPolicyObject::GetPath
author: windows-sdk-content
description: The GetPath method retrieves the path to the GPO.
old-location: policy\igrouppolicyobject_getpath.htm
tech.root: Policy
ms.assetid: ecfecaa4-eb6e-4de6-a5fe-ecd0e9df886c
ms.author: windowssdkdev
ms.date: 09/26/2018
ms.keywords: GetPath, GetPath method [Group Policy], GetPath method [Group Policy],IGroupPolicyObject interface, IGroupPolicyObject interface [Group Policy],GetPath method, IGroupPolicyObject.GetPath, IGroupPolicyObject::GetPath, _win32_igrouppolicyobject_getpath, gpedit/IGroupPolicyObject::GetPath, policy.igrouppolicyobject_getpath
ms.prod: windows-hardware
ms.technology: windows-devices
ms.topic: method
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
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IGroupPolicyObject.GetPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
---

# IGroupPolicyObject::GetPath


## -description


The
    <b>GetPath</b> method retrieves the path to the GPO.


## -parameters




### -param pszPath [out]

Pointer to a buffer that receives the path. If the GPO is an Active Directory object, the path is in ADSI name format. If the GPO is a computer object, this parameter receives a file system path.


### -param cchMaxLength

TBD




#### - cchMaxPath [in]

Specifies the maximum number of characters that can be stored in the <i>pszPath</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/0d6d0b3d-5ad4-4363-a123-f074193b75e2">GetDSPath</a>



<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/b3cd31a1-c238-4eb2-8164-9c4891e6227b">IGroupPolicyObject</a>
 

 

