---
UID: NF:gpedit.IRSOPInformation.GetNamespace
title: IRSOPInformation::GetNamespace
author: windows-sdk-content
description: The GetNameSpace method retrieves the namespace from which the RSoP data is being displayed.
old-location: policy\irsopinformation_getnamespace.htm
old-project: policy
ms.assetid: 3575072c-88d7-482c-bc8b-dca9f6d68577
ms.author: windowssdkdev
ms.date: 05/31/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetNameSpace method [Group Policy], GetNameSpace method [Group Policy],IRSOPInformation interface, GetNamespace, IRSOPInformation interface [Group Policy],GetNameSpace method, IRSOPInformation.GetNamespace, IRSOPInformation::GetNameSpace, IRSOPInformation::GetNamespace, _win32_irsopinformation_getnamespace, gpedit/IRSOPInformation::GetNameSpace, policy.irsopinformation_getnamespace
ms.prod: windows
ms.technology: windows-sdk
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
tech.root: 
req.typenames: 
topic_type:
 - APIRef
 - kbSyntax
api_type:
 - COM
api_location:
 - Gpedit.dll
api_name:
 - IRSOPInformation.GetNameSpace
product: Windows
targetos: Windows
req.lib: 
req.dll: Gpedit.dll
req.irql: 
req.product: GDI+ 1.1
---

# IRSOPInformation::GetNamespace


## -description


The
    <b>GetNameSpace</b> method retrieves the namespace from which the RSoP data is being displayed.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section


### -param pszName [out]

Receives the namespace from which the RSoP data is being displayed. The computer and user RSoP data are in sub-namespaces under this namespace. Computer RSoP data is under the Computer sub-namespace, and user RSoP data is under the User sub-namespace.


### -param cchMaxLength [in]

Specifies the size, in characters, of the <i>pszName</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -see-also




<a href="https://msdn.microsoft.com/dc15a69d-a44d-4731-a9e5-6165abd581c4">Group Policy
    Interfaces</a>



<a href="https://msdn.microsoft.com/1285ab5a-ea68-4c16-bc34-8ab2f3cfad35">Group Policy
    Overview</a>



<a href="https://msdn.microsoft.com/e3662977-d7a7-47bc-989b-a820d4c05382">IRSOPInformation</a>
 

 

