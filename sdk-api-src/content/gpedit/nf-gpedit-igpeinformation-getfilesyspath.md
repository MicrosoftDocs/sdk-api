---
UID: NF:gpedit.IGPEInformation.GetFileSysPath
title: IGPEInformation::GetFileSysPath (gpedit.h)
author: windows-sdk-content
description: The GetFileSysPath method returns the file system path for the specified section of the GPO. The path is in UNC format.
old-location: policy\igpeinformation_getfilesyspath.htm
tech.root: Policy
ms.assetid: 6fcdc7f8-61bf-4d3e-b0aa-ff730d6730cb
ms.author: windowssdkdev
ms.date: 12/05/2018
ms.keywords: GPO_SECTION_MACHINE, GPO_SECTION_ROOT, GPO_SECTION_USER, GetFileSysPath, GetFileSysPath method [Group Policy], GetFileSysPath method [Group Policy],IGPEInformation interface, IGPEInformation interface [Group Policy],GetFileSysPath method, IGPEInformation.GetFileSysPath, IGPEInformation::GetFileSysPath, _win32_igpeinformation_getfilesyspath, gpedit/IGPEInformation::GetFileSysPath, policy.igpeinformation_getfilesyspath
ms.topic: method
f1_keywords: 
 - "gpedit/IGPEInformation.GetFileSysPath"
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
 - IGPEInformation.GetFileSysPath
product: Windows
targetos: Windows
req.typenames: 
req.redist: 
ms.custom: 19H1
---

# IGPEInformation::GetFileSysPath


## -description


The
    <b>GetFileSysPath</b> method returns the file system path for the specified section of the GPO. The path is in UNC format.


## -parameters




### -param dwSection [in]

Specifies the GPO section. This parameter can be one of the following values.



#### GPO_SECTION_ROOT

Root section



#### GPO_SECTION_USER

User section



#### GPO_SECTION_MACHINE

Computer section


### -param pszPath [out]

Receives the file system path.


### -param cchMaxPath [in]

Specifies the size, in characters, of the <i>pszPath</i> buffer.


## -returns



If the method succeeds, the return value is <b>S_OK</b>. Otherwise, the method returns one of the COM error codes defined in the Platform SDK header file WinError.h.




## -remarks



To retrieve the Active Directory path for the specified section of a GPO, you can call the 
<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdspath">GetDSPath</a> method.




## -see-also




<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nf-gpedit-igpeinformation-getdspath">GetDSPath</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/group-policy-interfaces">Group Policy
    Interfaces</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/Policy/about-group-policy">Group Policy
    Overview</a>



<a href="https://docs.microsoft.com/previous-versions/windows/desktop/api/gpedit/nn-gpedit-igpeinformation">IGPEInformation</a>
 

 

